# On-demand Shadowsocks VPN via AWS copilot

You can easily spin up containerized, lightweight, and secured SOCKS5 proxy on Amazon ECS on AWS Fargate using [AWS Copilot](https://aws.github.io/copilot-cli/). Destroy it when you are done and only pay for what you use.

This guide is created for OSX users.

## Installation

1. Follow the [Installation](https://aws.github.io/copilot-cli/docs/getting-started/install/) docs to install AWS Copilot CLI.

2. Setup your [AWS Credentials](https://aws.github.io/copilot-cli/docs/credentials/)

3. Clone this repository 
`git clone git@github.com:rvelic/shadowsocks-copilot.git && cd shadowsocks-copilot`

## Usage

1. `copilot app init`
2. `copilot env deploy --name production`
3. `copilot svc deploy --app shadowsocks --env production --name libev`

You can check your running service and its status with `copilot svc show` and `copilot svc status`


## Cleanup

To delete everything run `copilot app delete`

## Thanks

To the awesome people at [shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev) and [AWS Copilot](https://aws.github.io/copilot-cli)