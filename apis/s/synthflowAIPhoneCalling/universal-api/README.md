# <img src="https://images.mindcloud.co/apps/icons/images-20_1776193561668.png" alt="Synthflow AI Phone Calling logo" width="28" height="28"> Synthflow AI Phone Calling: Universal API

Manage AI phone-calling workflows in Synthflow, including contacts, agents, calls, simulations, analytics, phone numbers, knowledge bases, and webhook logs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/synthflowAIPhoneCalling/latest
- **Category:** Support / Contact Center
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://synthflow.ai
- **Vendor API docs:** https://docs.synthflow.ai/reference/getting-started-with-your-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [List Actions](actions/list-actions.md) | GET | Retrieves all custom actions from Synthflow. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves a phone call from Synthflow. |
| [List Calls](actions/list-calls.md) | GET | Retrieves all phone calls from Synthflow. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Synthflow. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Synthflow. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from your Synthflow workspace. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contacts from your Synthflow workspace. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Synthflow. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Phone Book](actions/create-phone-book.md) | POST | Creates a new phone book in Synthflow. |
| [Delete Phone Book](actions/delete-phone-book.md) | DELETE | Deletes an existing phone book from Synthflow. |
| [List Phone Books](actions/list-phone-books.md) | GET | Retrieves all phone books from Synthflow. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Number](actions/get-phone-number.md) | GET | Retrieves a phone number from Synthflow. |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves all phone numbers from Synthflow. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new voice agent in Synthflow. |
| [Create Phone Book Entry](actions/create-phone-book-entry.md) | POST | Creates a new phone book entry in Synthflow. |
| [Create Simulation Case](actions/create-simulation-case.md) | POST | Creates a new simulation case in Synthflow. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing voice agent from Synthflow. |
| [Delete Phone Book Entry](actions/delete-phone-book-entry.md) | DELETE | Deletes an existing phone book entry from Synthflow. |
| [Delete Simulation Case](actions/delete-simulation-case.md) | DELETE | Deletes an existing simulation case from Synthflow. |
| [Generate Test Cases](actions/generate-test-cases.md) | POST | Generates new simulation cases in Synthflow. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves a voice agent from Synthflow. |
| [Get Simulation](actions/get-simulation.md) | GET | Retrieves a simulation run from Synthflow. |
| [Get Simulation Case](actions/get-simulation-case.md) | GET | Retrieves a simulation case from Synthflow. |
| [Get Simulation Session](actions/get-simulation-session.md) | GET | Retrieves a simulation session from Synthflow. |
| [List Agents](actions/list-agents.md) | GET | Retrieves all voice agents from Synthflow. |
| [List Simulation Cases](actions/list-simulation-cases.md) | GET | Retrieves all simulation cases from Synthflow. |
| [List Simulation Cases By Agent](actions/list-simulation-cases-by-agent.md) | GET | Retrieves simulation cases for a Synthflow agent. |
| [List Simulation Sessions](actions/list-simulation-sessions.md) | GET | Retrieves all simulation sessions from Synthflow. |
| [List Simulations](actions/list-simulations.md) | GET | Retrieves all simulation runs from Synthflow. |
| [Start Simulation](actions/start-simulation.md) | POST | Starts a new simulation in Synthflow. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing voice agent in Synthflow. |
| [Update Simulation Case](actions/update-simulation-case.md) | PUT | Updates an existing simulation case in Synthflow. |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Log](actions/get-webhook-log.md) | GET | Retrieves a webhook log from Synthflow. |
| [List Webhook Logs](actions/list-webhook-logs.md) | GET | Retrieves all webhook logs from Synthflow. |

