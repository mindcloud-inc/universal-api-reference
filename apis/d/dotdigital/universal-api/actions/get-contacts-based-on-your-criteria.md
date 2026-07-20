# Dotdigital: Get Contacts Based on Your Criteria

Finds contacts in Dotdigital by selected criteria.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-contacts-based-on-your-criteria
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-contacts-based-on-your-criteria?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-contacts-based-on-your-criteria?${params}`, {
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
| `dataFields` | string | no | Pipe-delimited contact data field keys to return, or [[ALL]] to return all data fields. Accepts multiple values in one string, delimited by `\|`. Example: `FIRSTNAME`. |
| `include` | list<string> | no | Additional contact datasets to include in the response. One of: `channelProperties`, `consentRecords`, `lists`, `preferences`. Accepts multiple values in one string, delimited by `\|`. |
| `created` | string | no | Use gte::YYYY-MM-DDTHH:MM:SSZ to filter by created date. Do not use with Modified Filter. Example: `gte::2021-12-17T00:00:00Z`. |
| `modified` | string | no | Use gte::YYYY-MM-DDTHH:MM:SSZ to filter by modified date. Example: `gte::2021-12-17T00:00:00Z`. |
| `listId` | number | no | Filter to a specific list. Do not use with Segment ID Filter. Example: `12345`. |
| `segmentId` | number | no | Filter to a specific segment. Do not use with List ID Filter. Example: `12345`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotdigital API returns.

## Native endpoint

Through the native Dotdigital API, this operation is `GET /contacts/v3` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contacts-based-on-your-criteria.md) for the provider-specific parameters and requirements.

