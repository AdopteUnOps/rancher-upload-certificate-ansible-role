# docker-ansible-role

Upload certificate into rancher environment.
By default it can generate selfsigned certificate

Mandatory Variables
--------------

```
common_name: "mydomain.com"
certificate_folder: "{{ inventory_dir }}/certificates/{{rancher_project_name}}"
```

Role Variables
--------------

```
subj_alt_names: []
generate_self_signed_certificate: true
key_size: 2048
days: 365

private_key_file: "{{certificate_folder}}/{{key_name}}.key"
csr_file: "{{certificate_folder}}/{{key_name}}.csr"
certificate_file:  "{{certificate_folder}}/{{key_name}}.crt"
ca_certificate_file:  "{{ inventory_dir }}/certificates/ca.crt"

rancher_master_url: "http://localhost:8080"
rancher_project_name: "default"
```
License
-------

Apache License 2
