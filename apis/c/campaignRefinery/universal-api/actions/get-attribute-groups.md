# Campaign Refinery: Get Attribute Groups

Retrieves attribute groups from Campaign Refinery.

```
GET https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-attribute-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-attribute-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-attribute-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_attr_group_created_dts": "2026-05-07T12:00:00.000Z",
      "custom_attr_group_id": 1,
      "custom_attr_group_name": "Ava Chen",
      "custom_attr_group_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_attr_group_created_dts` | date | Attribute group creation timestamp. |
| `custom_attr_group_id` | number | Campaign Refinery numeric attribute group ID. |
| `custom_attr_group_name` | string | Attribute group name. |
| `custom_attr_group_uuid` | string | Campaign Refinery attribute group UUID. |

## Native endpoint

Through the native Campaign Refinery API, this operation is `GET /attributes/get-attribute-groups` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attribute-groups.md) for the provider-specific parameters and requirements.

