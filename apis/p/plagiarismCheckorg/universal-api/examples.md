# PlagiarismCheck.org Universal API Examples

These examples use the MindCloud API key and PlagiarismCheck.org connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Plagiarism Text Before Submit



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "hash": "string",
      "pages": 1,
      "success": true,
      "warning": "string",
      "words": 1
    }
  ],
  "meta": {}
}
```

See the full [Validate Plagiarism Text Before Submit action reference](actions/validate-plagiarism-text-before-submit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit).

## Submit AI Check For B2B Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-ai-check-for-b2b-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "groupId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-ai-check-for-b2b-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "groupId": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Submit AI Check For B2B Group action reference](actions/submit-ai-check-for-b2b-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plagiarismCheckorg/latest/actions/submit-ai-check-for-b2b-group).
