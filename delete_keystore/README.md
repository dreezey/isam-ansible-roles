# Role Name

Use this Role to delete an existing keystore on the ISAM Appliance.

## Requirements

start_config role is a required dependencies. It contains the Ansible Custom Modules and handlers.

## Role Variables

The following variables are required:
* delete_keystore_id

## Dependencies

start_config role is a required dependencies. It contains the Ansible Custom Modules and handlers.

## Example Playbook

Here is an example on how to use this role:

    - name: Delete pdsrv on all hosts except primary master
      hosts: all,!primary_master
      connection: local
      roles:
        - start_config
        - role: delete_keystore
          delete_keystore_id: 'pdsrv'

## License

Apache

## Author Information

Dries Eestermans (dries.eestermans@is4u.be)
