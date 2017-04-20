# local-cl-mirror

An Ansible role that changes CloudLinux yum repository URLs to the specified local mirror.  
**Warning: that role is for CloudLinux OS development purposes only, don't use it in production.**

## Role Variables

Available variables and their default values are listed below:

* `local_cl_mirror_host: ''` - (**required**) a local mirror hostname.
* `local_cl_mirror_proto: 'http'` - connection protocol to use (e.g. https, ftp).
* `local_cl_mirror_testing_enabled: no` - enable or disable updates-testing repository.


## Example playbook

```yaml
    ---
    - hosts: all
      roles:
        - { role: ezamriy.local-cl-mirror,
            local_cl_mirror_host: 'example.com',
            local_cl_mirror_testing_enabled: yes }
```


## License

MIT


## Authors

* [Eugene Zamriy](https://github.com/ezamriy)
