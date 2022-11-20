# ansible-role-docker-container-guacamole

Role to run Guacamole in a docker container

## Table of content

- [Default Variables](#default-variables)
  - [docker_container_guacamole_admin_password](#docker_container_guacamole_admin_password)
  - [docker_container_guacamole_admin_username](#docker_container_guacamole_admin_username)
  - [docker_container_guacamole_ca_certificates](#docker_container_guacamole_ca_certificates)
  - [docker_container_guacamole_database_name](#docker_container_guacamole_database_name)
  - [docker_container_guacamole_database_password](#docker_container_guacamole_database_password)
  - [docker_container_guacamole_database_root_password](#docker_container_guacamole_database_root_password)
  - [docker_container_guacamole_database_user](#docker_container_guacamole_database_user)
  - [docker_container_guacamole_env](#docker_container_guacamole_env)
  - [docker_container_guacamole_image](#docker_container_guacamole_image)
  - [docker_container_guacamole_labels](#docker_container_guacamole_labels)
  - [docker_container_guacamole_ldap_admin_groupname](#docker_container_guacamole_ldap_admin_groupname)
  - [docker_container_guacamole_ldap_admin_username](#docker_container_guacamole_ldap_admin_username)
  - [docker_container_guacamole_ldap_enabled](#docker_container_guacamole_ldap_enabled)
  - [docker_container_guacamole_ldap_root_connection_groupname](#docker_container_guacamole_ldap_root_connection_groupname)
  - [docker_container_guacamole_mfa_enabled](#docker_container_guacamole_mfa_enabled)
  - [docker_container_guacamole_mfa_totp_issuer](#docker_container_guacamole_mfa_totp_issuer)
  - [docker_container_guacamole_mfa_totp_version](#docker_container_guacamole_mfa_totp_version)
  - [docker_container_guacamole_name](#docker_container_guacamole_name)
  - [docker_container_guacamole_networks](#docker_container_guacamole_networks)
  - [docker_container_guacamole_ports](#docker_container_guacamole_ports)
  - [docker_container_guacamole_restic_enable](#docker_container_guacamole_restic_enable)
  - [docker_container_guacamole_restic_retention](#docker_container_guacamole_restic_retention)
  - [docker_container_guacamole_restic_s3_bucket_name](#docker_container_guacamole_restic_s3_bucket_name)
  - [docker_container_guacamole_restic_s3_endpoint](#docker_container_guacamole_restic_s3_endpoint)
  - [docker_container_guacamole_restic_s3_repo](#docker_container_guacamole_restic_s3_repo)
  - [docker_container_guacamole_restic_s3_repo_access_key](#docker_container_guacamole_restic_s3_repo_access_key)
  - [docker_container_guacamole_restic_s3_repo_password](#docker_container_guacamole_restic_s3_repo_password)
  - [docker_container_guacamole_restic_s3_repo_secret_key](#docker_container_guacamole_restic_s3_repo_secret_key)
  - [docker_container_guacamole_restic_tag](#docker_container_guacamole_restic_tag)
  - [docker_container_guacamole_volume_dir](#docker_container_guacamole_volume_dir)
  - [docker_container_guacamole_volumes](#docker_container_guacamole_volumes)
  - [docker_container_guacamoledb_env](#docker_container_guacamoledb_env)
  - [docker_container_guacamoledb_image](#docker_container_guacamoledb_image)
  - [docker_container_guacamoledb_labels](#docker_container_guacamoledb_labels)
  - [docker_container_guacamoledb_name](#docker_container_guacamoledb_name)
  - [docker_container_guacamoledb_networks](#docker_container_guacamoledb_networks)
  - [docker_container_guacamoledb_ports](#docker_container_guacamoledb_ports)
  - [docker_container_guacamoledb_volume_dir](#docker_container_guacamoledb_volume_dir)
  - [docker_container_guacamoledb_volumes](#docker_container_guacamoledb_volumes)
  - [docker_container_guacd_env](#docker_container_guacd_env)
  - [docker_container_guacd_image](#docker_container_guacd_image)
  - [docker_container_guacd_labels](#docker_container_guacd_labels)
  - [docker_container_guacd_name](#docker_container_guacd_name)
  - [docker_container_guacd_networks](#docker_container_guacd_networks)
  - [docker_container_guacd_ports](#docker_container_guacd_ports)
  - [docker_container_guacd_volume_dir](#docker_container_guacd_volume_dir)
  - [docker_container_guacd_volumes](#docker_container_guacd_volumes)
  - [docker_image_guacamole_name](#docker_image_guacamole_name)
  - [docker_image_guacamole_pull](#docker_image_guacamole_pull)
  - [docker_image_guacamoledb_name](#docker_image_guacamoledb_name)
  - [docker_image_guacamoledb_pull](#docker_image_guacamoledb_pull)
  - [docker_image_guacd_name](#docker_image_guacd_name)
  - [docker_image_guacd_pull](#docker_image_guacd_pull)
  - [docker_network_guacamole_name](#docker_network_guacamole_name)
  - [docker_network_guacamoledb_name](#docker_network_guacamoledb_name)
  - [docker_network_guacd_name](#docker_network_guacd_name)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### docker_container_guacamole_admin_password

Initial admin password.

#### Default value

```YAML
docker_container_guacamole_admin_password: guacadmin
```

### docker_container_guacamole_admin_username

Initial admin username.

#### Default value

```YAML
docker_container_guacamole_admin_username: guacadmin
```

### docker_container_guacamole_ca_certificates

CA certificates used by Guacamole.

Example:

```yaml

docker_container_guacamole_ca_certificates:

- { cert_file: "files/acme1_org.cer" }

- { cert_file: "files/acme2_org.cer" }

```

#### Default value

```YAML
docker_container_guacamole_ca_certificates: []
```

### docker_container_guacamole_database_name

Name of the database.

#### Default value

```YAML
docker_container_guacamole_database_name: guacamole
```

### docker_container_guacamole_database_password

Password of the database user.

#### Default value

```YAML
docker_container_guacamole_database_password: guacsomethingsecret8888
```

### docker_container_guacamole_database_root_password

Root-Password of the database.

#### Default value

```YAML
docker_container_guacamole_database_root_password: guacsomethingsecret4444
```

### docker_container_guacamole_database_user

Name of the database user.

#### Default value

```YAML
docker_container_guacamole_database_user: guacamole
```

### docker_container_guacamole_env

Dictionery of key,value pairs for docker environment variables to configure guacamole.

#### Default value

```YAML
docker_container_guacamole_env:
  GUACAMOLE_HOME: /guac_home
  MYSQL_HOSTNAME: mysql
  MYSQL_DATABASE: '{{ docker_container_guacamole_database_name }}'
  MYSQL_USER: '{{ docker_container_guacamole_database_user }}'
  MYSQL_PASSWORD: '{{ docker_container_guacamole_database_password }}'
  GUACD_HOSTNAME: guacd
  GUACD_PORT: '4822'
  TOTP_ISSUER: '{{ docker_container_guacamole_mfa_totp_issuer }}'
  LDAP_HOSTNAME: '{{ docker_container_guacamole_ldap_hostame | default(omit) }}'
  LDAP_USER_BASE_DN: '{{ docker_container_guacamole_ldap_user_base_dn | default(omit)
    }}'
  LDAP_GROUP_BASE_DN: '{{ docker_container_guacamole_ldap_group_base_dn | default(omit)
    }}'
  LDAP_SEARCH_BIND_DN: '{{ docker_container_guacamole_ldap_search_bind_dn | default(omit)
    }}'
  LDAP_SEARCH_BIND_PASSWORD: '{{ docker_container_guacamole_ldap_search_bind_password
    | default(omit) }}'
  LDAP_PORT: "{{ docker_container_guacamole_ldap_port | default('389') }}"
  LDAP_ENCRYPTION_METHOD: "{{ docker_container_guacamole_ldap_encryption_method |\
    \ default('none') }}"
  LDAP_USERNAME_ATTRIBUTE: "{{ docker_container_guacamole_ldap_username_attribute\
    \ | default('userPrincipalName') }}"
  LDAP_GROUP_NAME_ATTRIBUTE: "{{ docker_container_guacamole_ldap_groupname_attribute\
    \ | default('cn') }}"
  LDAP_MEMBER_ATTRIBUTE: "{{ docker_container_guacamole_ldap_member_attribute | default('member')\
    \ }}"
  LDAP_USER_SEARCH_FILTER: "{{ docker_container_guacamole_ldap_user_search_filter\
    \ | default('(&(objectCategory=person)(objectclass=user)(!(userAccountControl:1.2.840.113556.1.4.803:=2)))')\
    \ }}"
```

### docker_container_guacamole_image

Repository path and tag used to create the container. If an image is not found or pull is true, the image will be pulled from the registry. If no tag is included, latest will be used.

#### Default value

```YAML
docker_container_guacamole_image: '{{ docker_image_guacamole_name }}'
```

### docker_container_guacamole_labels

Dictionary of key value pairs for container labels.

Example:

```yaml

docker_container_guacamole_labels:

traefik.enable: "true"

```

#### Default value

```YAML
docker_container_guacamole_labels: {}
```

### docker_container_guacamole_ldap_admin_groupname

Existing LDAP group. Members of this group get admin permissions.

#### Default value

```YAML
docker_container_guacamole_ldap_admin_groupname: guac_admins
```

### docker_container_guacamole_ldap_admin_username

Existing LDAP admin username. Choose the format acording to `docker_container_guacamole_ldap_username_attribute`

#### Default value

```YAML
docker_container_guacamole_ldap_admin_username: guac_admin@acme.org
```

### docker_container_guacamole_ldap_enabled

Enable LDAP authentication.

#### Default value

```YAML
docker_container_guacamole_ldap_enabled: false
```

### docker_container_guacamole_ldap_root_connection_groupname

Display name for Root Connection Group

#### Default value

```YAML
docker_container_guacamole_ldap_root_connection_groupname: ACME
```

### docker_container_guacamole_mfa_enabled

Enable TOTP authentication extension.

#### Default value

```YAML
docker_container_guacamole_mfa_enabled: false
```

### docker_container_guacamole_mfa_totp_issuer

Issue display name for TOTP authentication.

#### Default value

```YAML
docker_container_guacamole_mfa_totp_issuer: guacamole
```

### docker_container_guacamole_mfa_totp_version

TOTP authentication extensions version.

#### Default value

```YAML
docker_container_guacamole_mfa_totp_version: 1.4.0
```

### docker_container_guacamole_name

Name for the container

#### Default value

```YAML
docker_container_guacamole_name: guacamole
```

### docker_container_guacamole_networks

List of networks the container belongs to.

#### Default value

```YAML
docker_container_guacamole_networks:
  - name: '{{ docker_network_guacamole_name }}'
    links:
      - '{{ docker_container_guacamoledb_name }}:mysql'
      - '{{ docker_container_guacd_name }}:guacd'
```

### docker_container_guacamole_ports

List of ports to publish from the container to the host.

#### Default value

```YAML
docker_container_guacamole_ports:
  - 8080:8080
```

### docker_container_guacamole_restic_enable

Enable restic backup for the container's mounted volumes.

#### Default value

```YAML
docker_container_guacamole_restic_enable: false
```

### docker_container_guacamole_restic_retention

Retention settions for `restic forget` after the `restic backup`.

#### Default value

```YAML
docker_container_guacamole_restic_retention:
  keep_last: 1
  keep_daily: 7
  keep_weekly: 4
```

### docker_container_guacamole_restic_s3_bucket_name

Minio S3 bucket name for restic backup storage.

#### Default value

```YAML
docker_container_guacamole_restic_s3_bucket_name: restic-{{ docker_container_guacamole_name
  }}
```

### docker_container_guacamole_restic_s3_endpoint

Minio S3 endpoint for restic backup storage.

Example:

```yaml

docker_container__base__restic_s3_endpoint: "https://minio.{{ dns_domain }}"

docker_container_guacamole_restic_s3_endpoint: "{{ docker_container__base__restic_s3_endpoint }}"

```

#### Default value

```YAML
docker_container_guacamole_restic_s3_endpoint: '{{ docker_container__base__restic_s3_endpoint
  }}'
```

### docker_container_guacamole_restic_s3_repo

Minio S3 repo URL for restic backup storage.

#### Default value

```YAML
docker_container_guacamole_restic_s3_repo: s3:{{ docker_container_guacamole_restic_s3_endpoint
  }}/{{ docker_container_guacamole_restic_s3_bucket_name }}
```

### docker_container_guacamole_restic_s3_repo_access_key

Minio S3 repo access key for restic backup storage.

#### Default value

```YAML
docker_container_guacamole_restic_s3_repo_access_key: '{{ docker_container__base__restic_s3_repo_access_key
  }}'
```

### docker_container_guacamole_restic_s3_repo_password

Minio S3 repo password for restic backup storage.

#### Default value

```YAML
docker_container_guacamole_restic_s3_repo_password: '{{ docker_container__base__restic_s3_repo_password
  }}'
```

### docker_container_guacamole_restic_s3_repo_secret_key

Minio S3 repo secret key for restic backup storage.

#### Default value

```YAML
docker_container_guacamole_restic_s3_repo_secret_key: '{{ docker_container__base__restic_s3_repo_secret_key
  }}'
```

### docker_container_guacamole_restic_tag

Tag for the `restic backup` command

#### Default value

```YAML
docker_container_guacamole_restic_tag: '{{ docker_container_guacamole_name }}'
```

### docker_container_guacamole_volume_dir

Volume mount host directory, where Treafik config files are stored.

#### Default value

```YAML
docker_container_guacamole_volume_dir: '{{ docker_container__base__volume_dir }}/{{
  docker_container_guacamole_name }}'
```

### docker_container_guacamole_volumes

List of volumes to mount within the container.

#### Default value

```YAML
docker_container_guacamole_volumes:
  - '{{ docker_container_guacamole_volume_dir }}/conf/server.xml:/usr/local/tomcat/conf/server.xml'
  - '{{ docker_container_guacamole_volume_dir }}/home:/guac_home'
  - '{{ docker_container_guacamole_volume_dir }}/certs:/guac_certs'
```

### docker_container_guacamoledb_env

Dictionery of key,value pairs for docker environment variables to configure guacamoledb.

#### Default value

```YAML
docker_container_guacamoledb_env:
  MYSQL_ROOT_PASSWORD: '{{ docker_container_guacamole_database_root_password }}'
  MYSQL_DATABASE: '{{ docker_container_guacamole_database_name }}'
  MYSQL_USER: '{{ docker_container_guacamole_database_user }}'
  MYSQL_PASSWORD: '{{ docker_container_guacamole_database_password }}'
```

### docker_container_guacamoledb_image

Repository path and tag used to create the container. If an image is not found or pull is true, the image will be pulled from the registry. If no tag is included, latest will be used.

#### Default value

```YAML
docker_container_guacamoledb_image: '{{ docker_image_guacamoledb_name }}'
```

### docker_container_guacamoledb_labels

Dictionary of key value pairs for container labels.

Example:

```yaml

docker_container_guacamoledb_labels:

traefik.enable: "true"

```

#### Default value

```YAML
docker_container_guacamoledb_labels: {}
```

### docker_container_guacamoledb_name

Name for the container

#### Default value

```YAML
docker_container_guacamoledb_name: guacamoledb
```

### docker_container_guacamoledb_networks

List of networks the container belongs to.

#### Default value

```YAML
docker_container_guacamoledb_networks:
  - name: '{{ docker_network_guacamoledb_name }}'
```

### docker_container_guacamoledb_ports

List of ports to publish from the container to the host.

#### Default value

```YAML
docker_container_guacamoledb_ports: []
```

### docker_container_guacamoledb_volume_dir

Volume mount host directory, where Treafik config files are stored.

#### Default value

```YAML
docker_container_guacamoledb_volume_dir: '{{ docker_container__base__volume_dir }}/{{
  docker_container_guacamole_name }}'
```

### docker_container_guacamoledb_volumes

List of volumes to mount within the container.

#### Default value

```YAML
docker_container_guacamoledb_volumes:
  - '{{ docker_container_guacamole_volume_dir }}/mysql:/var/lib/mysql'
  - '{{ docker_container_guacamole_volume_dir }}/mysql_init/schema.sql:/docker-entrypoint-initdb.d/schema.sql:ro'
```

### docker_container_guacd_env

Dictionery of key,value pairs for docker environment variables to configure guacd.

#### Default value

```YAML
docker_container_guacd_env: {}
```

### docker_container_guacd_image

Repository path and tag used to create the container. If an image is not found or pull is true, the image will be pulled from the registry. If no tag is included, latest will be used.

#### Default value

```YAML
docker_container_guacd_image: '{{ docker_image_guacd_name }}'
```

### docker_container_guacd_labels

Dictionary of key value pairs for container labels.

Example:

```yaml

docker_container_guacd_labels:

traefik.enable: "true"

```

#### Default value

```YAML
docker_container_guacd_labels: {}
```

### docker_container_guacd_name

Name for the container

#### Default value

```YAML
docker_container_guacd_name: guacd
```

### docker_container_guacd_networks

List of networks the container belongs to.

#### Default value

```YAML
docker_container_guacd_networks:
  - name: '{{ docker_network_guacd_name }}'
```

### docker_container_guacd_ports

List of ports to publish from the container to the host.

#### Default value

```YAML
docker_container_guacd_ports: []
```

### docker_container_guacd_volume_dir

Volume mount host directory, where Treafik config files are stored.

#### Default value

```YAML
docker_container_guacd_volume_dir: '{{ docker_container__base__volume_dir }}/{{ docker_container_guacamole_name
  }}'
```

### docker_container_guacd_volumes

List of volumes to mount within the container.

#### Default value

```YAML
docker_container_guacd_volumes: []
```

### docker_image_guacamole_name

Repository path and tag for the container image.

#### Default value

```YAML
docker_image_guacamole_name: guacamole/guacamole:1.4.0
```

### docker_image_guacamole_pull

Indicate to always pull the docker image.

#### Default value

```YAML
docker_image_guacamole_pull: false
```

### docker_image_guacamoledb_name

Repository path and tag for the container image.

#### Default value

```YAML
docker_image_guacamoledb_name: mysql:8
```

### docker_image_guacamoledb_pull

Indicate to always pull the docker image.

#### Default value

```YAML
docker_image_guacamoledb_pull: false
```

### docker_image_guacd_name

Repository path and tag for the container image.

#### Default value

```YAML
docker_image_guacd_name: guacamole/guacd:1.4.0
```

### docker_image_guacd_pull

Indicate to always pull the docker image.

#### Default value

```YAML
docker_image_guacd_pull: false
```

### docker_network_guacamole_name

Name of the docker network created for guacamole.

#### Default value

```YAML
docker_network_guacamole_name: '{{ docker_container_guacamole_name }}_backend'
```

### docker_network_guacamoledb_name

Name of the docker network created for guacamoledb.

#### Default value

```YAML
docker_network_guacamoledb_name: '{{ docker_container_guacamole_name }}_backend'
```

### docker_network_guacd_name

Name of the docker network created for guacd.

#### Default value

```YAML
docker_network_guacd_name: '{{ docker_container_guacamole_name }}_backend'
```

## Discovered Tags

**_docker-container-backup-all_**\
&emsp;Backup all containers' volume mounts.

**_docker-container-backup-guacamole_**\
&emsp;Backup guacamole volume mounts.

**_docker-container-backup-init-all_**\
&emsp;Run init backup task for all container.

**_docker-container-backup-init-guacamole_**\
&emsp;Run init backup task for guacamole if restic is enabled.

**_docker-container-backup-list-all_**\
&emsp;List all containers' backups.

**_docker-container-backup-list-guacamole_**\
&emsp;List guacamole backups.

**_docker-container-prereq-all_**\
&emsp;Ensure all pre-requisites are installed

**_docker-container-prereq-guacamole_**\
&emsp;Ensure all pre-requisites for guacamole are installed

**_docker-container-purge-all_**\
&emsp;Remove all containers and delete volume mounts.

**_docker-container-purge-guacamole_**\
&emsp;Remove guacamole and delete volume mounts.

**_docker-container-remove-all_**\
&emsp;Remove all containers.

**_docker-container-remove-guacamole_**\
&emsp;Remove guacamole.

**_docker-container-restore-all_**\
&emsp;Run restic restore for all restic enabled containers.

**_docker-container-restore-guacamole_**\
&emsp;Run restic restore for guacamole if restic is enabled.

**_docker-container-setup-all_**\
&emsp;Run setup task for all containers.

**_docker-container-setup-guacamole_**\
&emsp;Run setup task for guacamole.

**_docker_container_guac_mfa_**

**_never_**


## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
