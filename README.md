# amazon-ssm-agent

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/cloudpunks/ansible-amazon-ssm-agent)
[![General Workflow](https://github.com/cloudpunks/ansible-amazon-ssm-agent/actions/workflows/general.yml/badge.svg)](https://github.com/cloudpunks/ansible-amazon-ssm-agent/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/cloudpunks/ansible-amazon-ssm-agent/actions/workflows/docs.yml/badge.svg)](https://github.com/cloudpunks/ansible-amazon-ssm-agent/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/cloudpunks/ansible-amazon-ssm-agent/actions/workflows/galaxy.yml/badge.svg)](https://github.com/cloudpunks/ansible-amazon-ssm-agent/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/cloudpunks/ansible-amazon-ssm-agent)](https://github.com/cloudpunks/ansible-amazon-ssm-agent/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/d/cloudpunks/amazon_ssm_agent)](https://galaxy.ansible.com/cloudpunks/amazon_ssm_agent)

Ansible role to install and configure Amazon SSM agent.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [amazon_ssm_agent_arch](#amazon_ssm_agent_arch)
  - [amazon_ssm_agent_package](#amazon_ssm_agent_package)
  - [amazon_ssm_agent_version](#amazon_ssm_agent_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### amazon_ssm_agent_arch

Architecture of the package to install

#### Default value

```YAML
amazon_ssm_agent_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64'
  }}"
```

### amazon_ssm_agent_package

Download URL for the package to install

#### Default value

```YAML
amazon_ssm_agent_package: https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/{{
  amazon_ssm_agent_version }}/debian_{{ amazon_ssm_agent_arch }}/amazon-ssm-agent.deb
```

### amazon_ssm_agent_version

Version of the release to install

#### Default value

```YAML
amazon_ssm_agent_version: latest
```

## Discovered Tags

**_amazon-ssm-agent_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Pascal Rimann](https://github.com/pascalrimann)
