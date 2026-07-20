# Add Subscriber Tag By Email with Maildroppa

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/tags/by-email`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Add Subscriber Tag By Email](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address of the subscriber whose tag is being created or removed. |
| `tagTypeId` | body | `string` | no | UUID of the TagType that is being associated with or removed from the subscriber. |
