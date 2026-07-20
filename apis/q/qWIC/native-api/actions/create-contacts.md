# Create Contacts with QWIC

Creates contacts in QWIC.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Create Contacts](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#creating-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<object>` | yes | List of contacts to create or update. Each contact object should include at least one of email or phone. |
