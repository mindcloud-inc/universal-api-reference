# Universe: List Event Questions

Retrieves attendee questions for a specific Universe event.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-questions?connectionId=$CONNECTION_ID&query=query%20ListEventQuestions(%24eventId%3A%20ID!)%20%7B%0A%20%20event(id%3A%20%24eventId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20title%0A%20%20%20%20questions%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20question%0A%20%20%20%20%20%20type%0A%20%20%20%20%20%20subType%0A%20%20%20%20%20%20required%0A%20%20%20%20%20%20included%0A%20%20%20%20%20%20multiple%0A%20%20%20%20%20%20hasOther%0A%20%20%20%20%20%20index%0A%20%20%20%20%20%20context%0A%20%20%20%20%20%20selectOptions%0A%20%20%20%20%20%20rateIds%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListEventQuestions($eventId: ID!) {\n  event(id: $eventId) {\n    id\n    title\n    questions {\n      id\n      question\n      type\n      subType\n      required\n      included\n      multiple\n      hasOther\n      index\n      context\n      selectOptions\n      rateIds\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-questions?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query ListEventQuestions($eventId: ID!) {\n  event(id: $eventId) {\n    id\n    title\n    questions {\n      id\n      question\n      type\n      subType\n      required\n      included\n      multiple\n      hasOther\n      index\n      context\n      selectOptions\n      rateIds\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for the event questions query. Default: `{"eventId":"69bc5bb99abe4b003ceea74f"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-questions.md) for the provider-specific parameters and requirements.

