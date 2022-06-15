---
title: "ID {{ .Name | title }}"
date: {{ .Date }}
draft: true
---
Sensor with CONNECTIVITY connectivity.

## Battery voltage

{{< thingspeak channel="CHANNEL_ID" chart="1" >}}

## Location

{{< swisstopo e="E_COORD" n="N_COORD" >}}