# ShareFile: Get Zone



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-zone?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-zone?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ShareFile zone identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "HeartBeatTolerance": 1,
      "Id": "string",
      "IsHIPAAZone": true,
      "IsMultiTenant": true,
      "Name": "Ava Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "url": "https://example.com",
      "Version": "string",
      "ZoneServices": "string",
      "ZoneType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `HeartBeatTolerance` | number | The zone heartbeat tolerance. |
| `Id` | string | The ShareFile zone identifier. |
| `IsHIPAAZone` | boolean | Whether the zone is HIPAA-enabled. |
| `IsMultiTenant` | boolean | Whether the zone is multi-tenant. |
| `Name` | string | The ShareFile zone name. |
| `odata.metadata` | string | The OData metadata URL for the returned zone. |
| `odata.type` | string | The OData type for the returned zone. |
| `url` | string | The API URL for the returned zone. |
| `Version` | string | The zone version. |
| `ZoneServices` | string | The enabled services for the zone. |
| `ZoneType` | string | The ShareFile zone type. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Zones({{id}})` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zone.md) for the provider-specific parameters and requirements.

