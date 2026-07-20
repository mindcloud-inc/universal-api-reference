# Create Sending Domain with SparkPost

## Endpoint

- **Method:** `POST`
- **Path:** `/sending-domains`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Create Sending Domain](https://developers.sparkpost.com/api/sending-domains/#sending-domains-post-create-a-sending-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Sending domain to create. |
| `tracking_domain` | body | `string` | no | Associated tracking domain. |
