# docker-ansible-role

Upload certificate into rancher environment.
By default it can generate selfsigned certificate

Mandatory Variables
--------------

```
common_name: "mydomain.com"
key_name: "mycert"
certificate_folder: "{{ inventory_dir }}/certificates/{{rancher_project_name}}"
rancher_api_key: "mykey"
rancher_api_secret: "mysecret"
rancher_project_name: "default"
rancher_project_id: 1234
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
ca_certificate_file:  "ca.crt"

rancher_master_url: "http://localhost:8080"

```
License
-------

Apache License 2
