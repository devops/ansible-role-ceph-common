# Role Name: ceph-common

A Ansible role for ceph common configure.

## Requirements

None.

## Role Variables

### `defaults/main.yml'`

* `ceph_repo_enable: False`
* `ceph_repo_baseurl: "http://download.ceph.com/rpm-firefly/el7/"`
* `ceph_cluster_name: "ceph"`
* `ceph_fsid: "80605375-25ef-46b0-afee-97aff959463f"`
* `ceph_mon_members: "{{ hostvars[groups['ceph-mon'][0]]['ansible_hostname'] }}, {{ hostvars[groups['ceph-mon'][1]]['ansible_hostname'] }}, {{ hostvars[groups['ceph-mon'][2]]['ansible_hostname'] }}"`
* `cep_mon_host: "10.0.2.31,10.0.2.32,10.0.2.33"`
* `ceph_public_network: "10.0.2.0/24"`
* `ceph_cluster_network: "10.0.3.0/24"`

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Ceph Node Base Configure.
      hosts: ceph
      roles:
        - role: ansible-role-ceph-common

## Author Information

z.
