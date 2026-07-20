# Send MMS with ExpertTexting

Creates an MMS message in ExpertTexting.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExptRestAPI/json/mms/send`
- **Base URL:** `https://www.experttexting.com`
- **Official documentation:** [Send MMS](https://www.experttexting.com/appv2/Documentation/SendMMS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Paid ExpertTexting MMS-enabled number purchased on your account. |
| `to` | body | `string` | yes | Recipient number in international format. |
| `text` | body | `string` | no | Optional MMS body text. |
| `mediaUrls` | body | `string` | yes | One or more publicly reachable JPG, JPEG, GIF, or PNG URLs for the MMS payload. |
