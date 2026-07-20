# Pipedream Utils: Formatting - [Text] Extract by Regular Expression

Extracts regex matches from text in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/extract-by-regular-expression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/extract-by-regular-expression?connectionId=$CONNECTION_ID&input=string&regExpString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "regExpString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/extract-by-regular-expression?${params}`, {
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
| `input` | string | yes | Text you would like to find a pattern from |
| `regExpString` | string | yes | Enter a string representing a [Regular Expression](https://www.w3schools.com/js/js_regexp.asp) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "endPosition": 1,
          "match": "string",
          "startPosition": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].endPosition` | number |  |
| `[].match` | string |  |
| `[].startPosition` | number |  |

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-by-regular-expression.md) for the provider-specific parameters and requirements.

