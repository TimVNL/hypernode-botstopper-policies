# Botstopper Policy Snippets for Hypernode

Reusable Botstopper policy snippets for Hypernode.

This repository contains small YAML snippets that can be added to the Botstopper policy files described in the Hypernode documentation:

https://docs.hypernode.com/hypernode-platform/botstopper/how-to-use-botstopper.html#how-to-use-botstopper-on-hypernode

## Overview

These snippets are not complete standalone Botstopper configurations. Each file is meant to be copied into one of the Botstopper policy files on your
Hypernode.

There are two types of snippets:

- `pre-*` snippets, which belong in
  `/data/web/botstopper/pre.policy.yml`
- `post-*` snippets, which belong in
  `/data/web/botstopper/post.policy.yml`

In short:

- if a filename starts with `pre-`, add it to `pre.policy.yml`
- if a filename starts with `post-`, add it to `post.policy.yml`

## Naming convention

Filenames indicate where a snippet should be used:

| Prefix  | Target file                            |
| ------- | -------------------------------------- |
| `pre-`  | `/data/web/botstopper/pre.policy.yml`  |
| `post-` | `/data/web/botstopper/post.policy.yml` |

### Examples:

- `pre-allow-cookiebot.yaml`
- `pre-allow-ohdear.yaml`
- `post-block-example.yaml`

The goal of this naming style is to make usage obvious at a glance.

## How to use these snippets

Using a snippet from this repository is straightforward:

1. Choose the snippet you want to use.
2. Check the filename prefix:
   - `pre-` means it belongs in `pre.policy.yml`
   - `post-` means it belongs in `post.policy.yml`
3. Open the matching Botstopper policy file on your Hypernode:
   - `/data/web/botstopper/pre.policy.yml`
   - `/data/web/botstopper/post.policy.yml`
4. Copy the contents of the snippet into the correct file.
5. Save the file.
6. Apply or reload the Botstopper configuration as described in the Hypernode
   documentation.
7. Test the result to confirm the rule behaves as expected.


## Important notes

Before applying any snippet, keep the following in mind:

- These files are snippets, not full Botstopper configurations
- `pre-*` files should only be added to `pre.policy.yml`
- `post-*` files should only be added to `post.policy.yml`
- When combining multiple snippets, make sure the final YAML remains valid
- Always test changes before applying them in production

## Disclaimer

These snippets are provided as examples and building blocks. Review and test
them carefully before use in production. A misconfigured Botstopper policy may
block legitimate traffic or allow unwanted traffic.

## Reference

- [Hypernode Botstopper documentation](
  https://docs.hypernode.com/hypernode-platform/botstopper/how-to-use-botstopper.html#how-to-use-botstopper-on-hypernode)
- [Anubis Policy Definitions](https://anubis.techaro.lol/docs/admin/policies)