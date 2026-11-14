# Infor ReserveCloud SCS: List Event Services



```
GET https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-event-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infor ReserveCloud SCS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-event-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-event-services?${params}`, {
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
| `filters` | string | no | Specify the uniqueId of a known record, a string field name, EQUAL_TO and a string value or a date field name, comparison operator and a date to filter the results. Operators: EQUAL_TO, NOT_EQUAL_TO, LESS_THAN, LESS_THAN_OR_EQUAL_TO, GREATER_THAN, GREATER_THAN_OR_EQUAL_TO Examples: filters=[['startDate','GREATER_THAN','07/01/2013'], ['startDate','LESS_THAN','12/31/2015']] filters=[['uniqueId','EQUAL_TO',' 8bd88078-ea60-438e8022-34b79ce26f08']] |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infor ReserveCloud SCS API returns.

## Native endpoint

Through the native Infor ReserveCloud SCS API, this operation is `GET https://www.reservecloud.com/gateway/request`. The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-services.md) for the provider-specific parameters and requirements.

