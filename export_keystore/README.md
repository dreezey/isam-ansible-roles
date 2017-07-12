# Role Name

Use this Role to export an existing keystore on the ISAM Appliance.

## Requirements

start_config role is a required dependencies. It contains the Ansible Custom Modules and handlers.

## Role Variables

The following variable is required:
* export_keystore_id
* export_keystore_filepath

## Dependencies

start_config role is a required dependencies. It contains the Ansible Custom Modules and handlers.

## Example Playbook

Here is an example on how to use this role:

    - name: Export pdsrv from primary_master
      hosts: primary_master
      connection: local
      roles:
        - start_config
        - role: export_keystore
          export_keystore_id: 'pdsrv'
          export_keystore_filepath: "/tmp/{{export_keystore_id}}-{{appliance_name}}" 

## License

Apache

## Author Information

Dries Eestermans (dries.eestermans@is4u.be)
