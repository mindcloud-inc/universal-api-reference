# List Launches with Launch Library 2

## Endpoint

- **Method:** `GET`
- **Path:** `launches/`
- **Base URL:** `https://ll.thespacedevs.com/2.3.0/`
- **Official documentation:** [List Launches](https://ll.thespacedevs.com/2.3.0/launches/?format=api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search launch designator, provider, mission, launch, pad, rocket, or spacecraft fields. |
| `mode` | query | `string` | no | Response detail level: list, normal, or detailed. Accepted values: `0`, `1`, `2`. |
