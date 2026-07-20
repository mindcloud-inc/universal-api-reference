# Add Email Domain with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/email/1/domains`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Add Email Domain](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | body | `string` | yes | Unique name for the domain. |
| `dkimKeyLength` | body | `string` | no | Value for DKIM key length. |
| `targetedDailyTraffic` | body | `number` | yes | Targeted daily traffic. |
| `applicationId` | body | `string` | no | Required for application use in a send request for outbound traffic. Returned in notification events. |
| `entityId` | body | `string` | no | Required for entity use in a send request for outbound traffic. Returned in notification events. |
