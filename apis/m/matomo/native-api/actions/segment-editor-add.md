# SegmentEditor add with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SegmentEditor add](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Matomo API parameter. |
| `definition` | body | `string` | yes | Matomo API parameter. |
| `?int idSite` | body | `string` | yes | Matomo API parameter. |
| `autoArchive` | body | `string` | no | Matomo API parameter. |
| `enabledAllUsers` | body | `boolean` | no | Matomo API parameter. |
