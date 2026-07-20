# Check Domain Reputation with OOPSpam

Checks a domain's reputation in OOPSpam.

## Endpoint

- **Method:** `POST`
- **Path:** `/reputation/domain`
- **Base URL:** `https://api.oopspam.com/v1`
- **Official documentation:** [Check Domain Reputation](https://www.oopspam.com/docs/#domain-reputation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Fully qualified domain name without protocol or www. |
