# Acknowledge Host Problems with Checkmk

Creates host problem acknowledgements in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/acknowledge/collections/host`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Acknowledge Host Problems](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/acknowledgement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | body | `string` | yes | Host whose problems should be acknowledged. |
| `comment` | body | `string` | yes | Acknowledgement comment. |
| `sticky` | body | `boolean` | no | Whether acknowledgements should be sticky. |
| `persistent` | body | `boolean` | no | Whether acknowledgements should persist. |
| `notify` | body | `boolean` | no | Whether Checkmk should notify contacts. |
