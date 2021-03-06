.. _aci_contract_subject:


aci_contract_subject - Manage initial Contract Subjects on Cisco ACI fabrics (vz:Subj)
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.4


.. contents::
   :local:
   :depth: 2


Synopsis
--------

* Manage initial Contract Subjects on Cisco ACI fabrics.
* More information from the internal APIC class *vz:Subj* at https://developer.cisco.com/media/mim-ref/MO-vzSubj.html.


Requirements (on host that executes module)
-------------------------------------------

  * ACI Fabric 1.0(3f)+


Options
-------

.. raw:: html

    <table border=1 cellpadding=4>

    <tr>
    <th class="head">parameter</th>
    <th class="head">required</th>
    <th class="head">default</th>
    <th class="head">choices</th>
    <th class="head">comments</th>
    </tr>

    <tr>
    <td>consumer_match<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>at_least_one</td>
    <td><ul><li>all</li><li>at_least_one</li><li>at_most_one</li><li>none</li></ul></td>
    <td>
        <div>The match criteria across consumers.</div>
        <div>The APIC defaults new Contract Subjects to <code>at_least_one</code>.</div>
    </td>
    </tr>

    <tr>
    <td>contract<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
    <td></td>
    <td>
        <div>The name of the Contract.</div>
        </br><div style="font-size: small;">aliases: contract_name</div>
    </td>
    </tr>

    <tr>
    <td>description<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
    <td></td>
    <td>
        <div>Description for the contract subject.</div>
    </td>
    </tr>

    <tr>
    <td>dscp<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>unspecified</td>
    <td><ul><li>AF11</li><li>AF12</li><li>AF13</li><li>AF21</li><li>AF22</li><li>AF23</li><li>AF31</li><li>AF32</li><li>AF33</li><li>AF41</li><li>AF42</li><li>AF43</li><li>CS0</li><li>CS1</li><li>CS2</li><li>CS3</li><li>CS4</li><li>CS5</li><li>CS6</li><li>CS7</li><li>EF</li><li>VA</li><li>unspecified</li></ul></td>
    <td>
        <div>The target DSCP.</div>
        <div>The APIC defaults new Contract Subjects to <code>unspecified</code>.</div>
        </br><div style="font-size: small;">aliases: target</div>
    </td>
    </tr>

    <tr>
    <td>hostname<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td>
        <div>IP Address or hostname of APIC resolvable by Ansible control host.</div>
        </br><div style="font-size: small;">aliases: host</div>
    </td>
    </tr>

    <tr>
    <td>password<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td>
        <div>The password to use for authentication.</div>
    </td>
    </tr>

    <tr>
    <td>priority<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>unspecified</td>
    <td><ul><li>level1</li><li>level2</li><li>level3</li><li>unspecified</li></ul></td>
    <td>
        <div>The QoS class.</div>
        <div>The APIC defaults new Contract Subjects to <code>unspecified</code>.</div>
    </td>
    </tr>

    <tr>
    <td>provider_match<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>at_least_one</td>
    <td><ul><li>all</li><li>at_least_one</li><li>at_most_one</li><li>none</li></ul></td>
    <td>
        <div>The match criteria across providers.</div>
        <div>The APIC defaults new Contract Subjects to <code>at_least_one</code>.</div>
    </td>
    </tr>

    <tr>
    <td>reverse_filter<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>True</td>
    <td><ul><li>True</li><li>False</li></ul></td>
    <td>
        <div>Determines if the APIC should reverse the src and dst ports to allow the return traffic back, since ACI is stateless filter.</div>
        <div>The APIC defaults new Contract Subjects to <code>yes</code>.</div>
    </td>
    </tr>

    <tr>
    <td>state<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>present</td>
    <td><ul><li>absent</li><li>present</li><li>query</li></ul></td>
    <td>
        <div>Use <code>present</code> or <code>absent</code> for adding or removing.</div>
        <div>Use <code>query</code> for listing an object or multiple objects.</div>
    </td>
    </tr>

    <tr>
    <td>subject<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
    <td></td>
    <td>
        <div>The contract subject name.</div>
        </br><div style="font-size: small;">aliases: contract_subject, name, subject_name</div>
    </td>
    </tr>

    <tr>
    <td>tenant<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
    <td></td>
    <td>
        <div>The name of the tenant.</div>
        </br><div style="font-size: small;">aliases: tenant_name</div>
    </td>
    </tr>

    <tr>
    <td>timeout<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>30</td>
    <td></td>
    <td>
        <div>The socket level timeout in seconds.</div>
    </td>
    </tr>

    <tr>
    <td>use_proxy<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>yes</td>
    <td><ul><li>yes</li><li>no</li></ul></td>
    <td>
        <div>If <code>no</code>, it will not use a proxy, even if one is defined in an environment variable on the target hosts.</div>
    </td>
    </tr>

    <tr>
    <td>use_ssl<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>yes</td>
    <td><ul><li>yes</li><li>no</li></ul></td>
    <td>
        <div>If <code>no</code>, an HTTP connection will be used instead of the default HTTPS connection.</div>
    </td>
    </tr>

    <tr>
    <td>username<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td>admin</td>
    <td></td>
    <td>
        <div>The username to use for authentication.</div>
        </br><div style="font-size: small;">aliases: user</div>
    </td>
    </tr>

    <tr>
    <td>validate_certs<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>yes</td>
    <td><ul><li>yes</li><li>no</li></ul></td>
    <td>
        <div>If <code>no</code>, SSL certificates will not be validated.</div>
        <div>This should only set to <code>no</code> used on personally controlled sites using self-signed certificates.</div>
    </td>
    </tr>

    </table>
    </br>



Examples
--------

 ::

    
    - name: Add a new contract subject
      aci_contract_subject:
        hostname: apic
        username: admin
        password: SomeSecretPassword
        tenant: production
        contract: web_to_db
        subject: default
        description: test
        reverse_filter: yes
        priority: level1
        dscp: unspecified
        state: present
    
    - name: Remove a contract subject
      aci_contract_subject:
        hostname: apic
        username: admin
        password: SomeSecretPassword
        tenant: production
        contract: web_to_db
        subject: default
        state: absent
    
    - name: Query a contract subject
      aci_contract_subject:
        hostname: apic
        username: admin
        password: SomeSecretPassword
        tenant: production
        contract: web_to_db
        subject: default
        state: query
    
    - name: Query all contract subjects
      aci_contract_subject:
        hostname: apic
        username: admin
        password: SomeSecretPassword
        state: query


Notes
-----

.. note::
    - The ``tenant`` and ``contract`` used must exist before using this module in your playbook.
    - The :ref:`aci_tenant <aci_tenant>` and :ref:`aci_contract <aci_contract>` modules can be used for this.
    - By default, if an environment variable ``<protocol>_proxy`` is set on the target host, requests will be sent through that proxy. This behaviour can be overridden by setting a variable for this task (see `setting the environment <http://docs.ansible.com/playbooks_environment.html>`_), or by using the ``use_proxy`` option.
    - HTTP redirects can redirect from HTTP to HTTPS so you should be sure that your proxy environment for both protocols is correct.



Status
~~~~~~

This module is flagged as **preview** which means that it is not guaranteed to have a backwards compatible interface.

For help in developing on modules, should you be so inclined, please read :doc:`community`, :doc:`dev_guide/testing` and :doc:`dev_guide/developing_modules`.
