# Apply Group Memberships with Zubie

Applies group memberships in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/apply`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Apply Group Memberships](https://developer.zubie.com/reference/groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | query | `string` | yes | The action to apply. One of add, remove, or replace. |
| `group_keys[]` | body | `array<string>` | yes | List of group keys to apply. |
| `member_keys[]` | body | `array<string>` | yes | List of member entity keys to act on. |
