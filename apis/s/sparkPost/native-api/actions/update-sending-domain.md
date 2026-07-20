# Update Sending Domain with SparkPost

## Endpoint

- **Method:** `PUT`
- **Path:** `/sending-domains/:domain`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Update Sending Domain](https://developers.sparkpost.com/api/sending-domains/#sending-domains-put-update-a-sending-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Sending domain to update. |
| `is_default_bounce_domain` | body | `boolean` | no | Whether this domain becomes the default bounce domain. |
| `shared_with_subaccounts` | body | `boolean` | no | Whether the sending domain can be shared with subaccounts. |
| `tracking_domain` | body | `string` | no | Associated tracking domain. |
