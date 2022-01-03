<img src="https://cdn.svgporn.com/logos/nodejs-icon.svg" width="20%" align="right" hspace="20" />

<h1 align="center">
  Ansible Role for <a href="https://nodejs.org/">NodeJS</a> via <a href="https://github.com/nvm-sh/nvm">NVM</a>
</h1>

<p>
  <a href="./LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" />
  </a>
</p>

> This repo contains a Linux-distro agnostic Ansible role that installs [NodeJS](https://nodejs.org/) using <a href="https://github.com/nvm-sh/nvm">NVM (Node Version Manager)</a>.

## Requirements

- No additional requirements.

- ⚠️ Note: the role does not change your profile files (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`). Make sure that you have added following to the profile file for automatic nvm loading:

  ```zsh
  export NVM_DIR="${HOME}/.nvm"
  [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
  ```

## Example Ansible Playbook

```yaml
- hosts: 127.0.0.1
  roles:
    - role: ansible-role-node
      vars:
        nvm_node_version: 16 # Node version needs to be installed.
        nvm_npm_global_packages: # NPM global packages list.
          - eslint
          - eslint-config-airbnb
          - eslint-config-google
```

## Author

👤 **Alexander Danilenko**

* Website: https://danilenko.in
* Github: [@alexander-danilenko](https://github.com/alexander-danilenko)
* LinkedIn: [@alexander-danilenko](https://linkedin.com/in/alexander-danilenko)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/alexander-danilenko/ansible-role-node/issues). 

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2022 [Alexander Danilenko](https://github.com/alexander-danilenko).<br />
This project is [MIT](./LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_