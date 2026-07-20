# eTermin: List Service Groups

Retrieves service groups from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-service-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-service-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-service-groups?${params}`, {
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
| `servicegroupid` | number | no | ID of the servicegroup that you want information on |
| `languageid` | string | no | Language code if you only want the information for a specific language e.g. DE, EN, etc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalTextDe": "string",
      "addTextDisplayMode": 1,
      "answerSelection": 1,
      "answerSortOrder": 1,
      "collapse": true,
      "countryLimitation": "string",
      "displayIndex": 1,
      "enabled": true,
      "isOptional": true,
      "isSimple": true,
      "nrServiceColumns": 1,
      "pageidx": 1,
      "regex": "string",
      "selMinDuration": 1,
      "selMinPrice": 1,
      "serviceGroupDe": "string",
      "serviceGroupType": 1,
      "showDuration": true,
      "showImgFull": true,
      "showInEmailSummary": true,
      "showInSummary": true,
      "showPrice": true,
      "showToggle": true,
      "showWhenCertainAnswerSelected": "string",
      "standardAnswerIndex": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalTextDe` | string |  |
| `addTextDisplayMode` | number |  |
| `answerSelection` | number |  |
| `answerSortOrder` | number |  |
| `collapse` | boolean |  |
| `countryLimitation` | string |  |
| `displayIndex` | number |  |
| `enabled` | boolean |  |
| `isOptional` | boolean |  |
| `isSimple` | boolean |  |
| `nrServiceColumns` | number |  |
| `pageidx` | number |  |
| `regex` | string |  |
| `selMinDuration` | number |  |
| `selMinPrice` | number |  |
| `serviceGroupDe` | string |  |
| `serviceGroupType` | number |  |
| `showDuration` | boolean |  |
| `showImgFull` | boolean |  |
| `showInEmailSummary` | boolean |  |
| `showInSummary` | boolean |  |
| `showPrice` | boolean |  |
| `showToggle` | boolean |  |
| `showWhenCertainAnswerSelected` | string |  |
| `standardAnswerIndex` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/servicegroup` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-groups.md) for the provider-specific parameters and requirements.

