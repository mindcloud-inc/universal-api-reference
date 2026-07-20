# Survalyzer: List Surveys



```
GET https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-surveys?${params}`, {
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
| `conditionOperator` | string | no | Comparison operator used by the provider filter. |
| `conditionType` | string | no | Provider filter object type to search. |
| `conjunction` | string | no | How multiple filters should be combined. |
| `identifier` | string | no | Field identifier used in the filter. |
| `page` | string | no | 1-based results page number. |
| `pageSize` | string | no | Maximum number of records to return. |
| `value` | string | no | Filter comparison value. |
| `workspaceId` | string | no | The Survalyzer workspace identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "surveys": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |
| `surveys` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Survey/v3/ReadSurveyList` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

