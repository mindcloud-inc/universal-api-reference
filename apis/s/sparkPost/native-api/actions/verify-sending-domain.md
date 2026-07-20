# Verify Sending Domain with SparkPost

## Endpoint

- **Method:** `POST`
- **Path:** `/sending-domains/:domain/verify`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Verify Sending Domain](https://developers.sparkpost.com/api/sending-domains/#sending-domains-post-verify-a-sending-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cname_verify` | body | `boolean` | no | Request CNAME verification. |
| `dkim_verify` | body | `boolean` | no | Request DKIM verification. |
| `domain` | path | `string` | yes | Sending domain to verify. |
