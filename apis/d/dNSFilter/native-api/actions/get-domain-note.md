# Get Domain Note with DNSFilter

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notes/:resource/:id/:domain`
- **Base URL:** `https://api.dnsfilter.com`
- **Official documentation:** [Get Domain Note](https://api.dnsfilter.com/docs#/paths/~1v1~1notes~1{resource}~1{id}~1{domain}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource` | path | `string` | yes | Valid resources: policies, msps or organizations |
| `id` | path | `number` | yes | Resource ID |
| `domain` | path | `string` | yes | Domain |
