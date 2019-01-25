---
layout: page
title: "Fritzbox"
description: "Instructions on how to integrate the AVM Fritzbox Smart Home components."
date: 2018-02-18 17:10
sidebar: true
comments: false
sharing: true
footer: true
logo: avm.png
ha_category: Hub
ha_release: 0.68
ha_iot_class: "Local Polling"
---

The [AVM](https://en.avm.de) Fritzbox component for Home Assistant allows you to integrate the switch and climate devices.

#### {% linkable_title Tested Devices %}

- [FRITZ!Box 6490 Cable](https://en.avm.de/products/fritzbox/fritzbox-6490-cable/)
- [FRITZ!Box 7590](https://en.avm.de/products/fritzbox/fritzbox-7590/)
- [FRITZ!DECT 200](https://en.avm.de/products/fritzdect/fritzdect-200/)
- [Eurotronic Comet DECT](https://eurotronic.org/produkte/elektronische-heizkoerperthermostate/sparmatic-comet/)


## {% linkable_title Setup %}

```yaml
# Example configuration.yaml entry
fritzbox:
  devices:
    - host: fritz.box
      username: YOUR_USERNAME
      password: YOUR_PASSWORD
```

{% configuration %}
devices:
  description: A list of Fritzbox devices.
  required: true
  type: map
  keys:
    host:
      description: The hostname or IP address of the Fritzbox.
      required: true
      type: string
    username:
      description: The username for Smart Home access.
      required: true
      type: string
    password:
      description: The password of the user.
      required: true
      type: string
{% endconfiguration %}

It is recommended to create a dedicated user for Home Assistant and only allow access to "Smart Home".

You also have to setup the user and password access to the FRITZ!Box user interface. 
Go to '*System > Fritz!Box Users > Login to the Home Network*' and set '*Registration in the Home Network*' to '*Every FRITZ!Box user logs in with his own user name and own password*'.
