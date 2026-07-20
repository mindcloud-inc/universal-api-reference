# Update Email Domain Tracking Events with Infobip

## Endpoint

- **Method:** `PUT`
- **Path:** `/email/1/domains/{domainName}/tracking`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Update Email Domain Tracking Events](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | path | `string` | yes | Domain for which the tracking events need to be updated. |
| `open` | body | `boolean` | no | Boolean value corresponding to whether opens for a message needs to be tracked or not. |
| `clicks` | body | `boolean` | no | Boolean value corresponding to whether clicks for a message needs to be tracked or not. |
| `unsubscribe` | body | `boolean` | no | Boolean value corresponding to whether unsubscribe for a message needs to be tracked or not. |
