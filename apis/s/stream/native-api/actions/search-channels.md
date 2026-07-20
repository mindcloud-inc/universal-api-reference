# Search Channels with Stream

Finds channels in Stream by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Search Channels](https://getstream.io/chat/docs/javascript/query_channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_conditions` | body | `object` | no | Channel query filter object. |
| `limit` | body | `number` | no | Maximum number of channels to return. |
| `offset` | body | `number` | no | Result offset for pagination. |
| `sort[]` | body | `array<object>` | no | Sort descriptors array. |
| `state` | body | `boolean` | no | Whether to include channel state. |
