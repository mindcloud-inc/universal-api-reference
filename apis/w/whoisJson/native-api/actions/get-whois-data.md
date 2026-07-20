# Get Whois Data with WhoisJson

Retrieves WHOIS data for a domain from WhoisJson.

## Endpoint

- **Method:** `GET`
- **Path:** `/whois`
- **Base URL:** `https://whoisjson.com/api/v1`
- **Official documentation:** [Get Whois Data](https://whoisjson.com/whois-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain name to look up. |
| `format` | query | `string` | no | Optional response format. WhoisJSON documents json and xml. |
