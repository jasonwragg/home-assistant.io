---
title: Steam
description: Instructions on how to set up Steam sensors in Home Assistant.
ha_category:
  - Social
ha_config_flow: true
ha_iot_class: Cloud Polling
ha_release: 0.14
ha_domain: steam_online
ha_platforms:
  - sensor
ha_codeowners:
  - '@tkdrob'
ha_integration_type: integration
ha_codeowners:
  - '@tkdrob'
ha_config_flow: true
---

The Steam integration will allow you to track the online status of public [Steam](https://steamcommunity.com) accounts.

{% include integrations/config_flow.md %}

## Setup

You need a [free API key](https://steamcommunity.com/dev/apikey) to use the platform.

To find an account's 64-bit SteamID on profiles without a custom URL you can check the URL of the profile page, the long string of numbers at the end is the 64-bit SteamID. If the profile has a custom URL you will have to copy the URL into [STEAMID I/O](https://steamid.io/) to find the 64-bit SteamID.

## Examples

If you want to add the accounts to a group for example you will have to use:

```yaml
# Example configuration.yaml entry
group:
  steam:
    name: Steam
    entities:
      - sensor.steam_account1
      - sensor.steam_account2
```
