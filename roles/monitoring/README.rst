.. versionadded:: 0.1

`Collectd <collectd https://collectd.org>`_ connects to
:doc:`mesos`, :doc:`docker` and host OS via Python modules, and collects their performance/health metrics which then are sent to specified logging host.

Variables
---------

.. data:: logging_host

   Host to receive collected metrics.

   default: ``{{ ansible_ssh_host }}``

.. data:: logging_host_port

   UDP port of logging_host

   default: ``25826``

.. data:: mesos_master_host

   Host to get Mesos master metrics port. 

   default: ``localhost``

.. data:: mesos_master_port

   Mesos master HTTP API port.

   default: ``15050``

.. data:: mesos_slave_host

   Host to get Mesos slave metrics port. 

   default: ``localhost``

.. data:: mesos_slave_port

   Mesos slave HTTP API port.

   default: ``15050``
          

  
.. _monitoring-example-playbook:


Example Playbook
----------------

.. code-block:: yaml+jinja

    ---
    - hosts: all
      roles:
        - monitoring

