# Wikibot Universal API Examples

These examples use the MindCloud API key and Wikibot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agents

Retrieves bot agents from Wikibot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/list-agents?${params}`, {
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
      "enabled": true,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wikibot/latest/actions/list-agents).

## Anonymize Text

Anonymizes text in Wikibot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/anonymize-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "Customer Ivan Petrov called from +7 999 123-45-67."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/anonymize-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "Customer Ivan Petrov called from +7 999 123-45-67."
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "anonymized_text": "string",
      "replacements": [
        {
          "entity_type": "string",
          "fake": "string",
          "ignored_names": "Ava Chen",
          "original": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Anonymize Text action reference](actions/anonymize-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wikibot/latest/actions/anonymize-text).
