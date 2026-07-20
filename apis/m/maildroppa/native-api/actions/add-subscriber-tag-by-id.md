# Add Subscriber Tag By ID with Maildroppa

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/tags/by-id`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Add Subscriber Tag By ID](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberId` | body | `string` | no | UUID of the subscriber whose tag is being created or removed. |
| `tagTypeId` | body | `string` | no | UUID of the TagType that is being associated with or removed from the subscriber. |
