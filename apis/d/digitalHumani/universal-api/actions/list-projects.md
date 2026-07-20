# Digital Humani: List Projects

Lists reforestation projects in Digital Humani.

```
GET https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/list-projects?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "reforestationCompanyName_en": "Ava Chen",
      "reforestationProjectCountry_en": "string",
      "reforestationProjectDescription_en": "string",
      "reforestationProjectState_en": "string",
      "reforestationProjectWebsite_en": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `reforestationCompanyName_en` | string |  |
| `reforestationProjectCountry_en` | string |  |
| `reforestationProjectDescription_en` | string |  |
| `reforestationProjectState_en` | string |  |
| `reforestationProjectWebsite_en` | string |  |

## Native endpoint

Through the native Digital Humani API, this operation is `GET /project` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

