# <img src="https://images.mindcloud.co/apps/icons/signal-wire_1774060660894.png" alt="SignalWire logo" width="28" height="28"> SignalWire: Universal API

Manage SignalWire calling, datasphere, fabric, fax, messaging, and voice resources from your SignalWire space.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signalWire/latest
- **Category:** Communication / Team Messaging
- **Actions:** 120
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://signalwire.com
- **Vendor API docs:** https://signalwire.com/docs/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Fabric Resources](actions/list-fabric-resources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-fabric-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (120)

### Ai Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Agent](actions/create-ai-agent.md) | POST | Creates a new AI agent in SignalWire. |
| [Delete AI Agent](actions/delete-ai-agent.md) | DELETE | Deletes an existing AI agent from SignalWire. |
| [Get AI Agent](actions/get-ai-agent.md) | GET | Retrieves an AI agent from SignalWire. |
| [List AI Agents](actions/list-ai-agents.md) | GET | Retrieves AI agents from SignalWire. |
| [Update AI Agent](actions/update-ai-agent.md) | PUT | Updates an existing AI agent in SignalWire. |

### Ai Agent Address

| Action | Method | Description |
| --- | --- | --- |
| [List AI Agent Addresses](actions/list-ai-agent-addresses.md) | GET | Retrieves AI agent addresses from SignalWire. |

### Assign A Resource As A Call Handler For A Domain Application.

| Action | Method | Description |
| --- | --- | --- |
| [Assign a resource as a call handler for a Domain Application.](actions/assign-a-resource-as-a-call-handler-for-a-domain-application.md) | PUT | Assigns a resource as a call handler for a domain application in SignalWire. |

### Assign A Resource To A Phone Route

| Action | Method | Description |
| --- | --- | --- |
| [Assign a Resource to a Phone Route](actions/assign-a-resource-to-a-phone-route.md) | PUT | Assigns a resource to a phone route in SignalWire. |

### Assign A Resource To A Sip Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Assign a Resource to a SIP endpoint](actions/assign-a-resource-to-a-sip-endpoint.md) | PUT | Assigns a resource to a SIP endpoint in SignalWire. |

### C Xml Application

| Action | Method | Description |
| --- | --- | --- |
| [Get cXML Application](actions/get-cxml-application.md) | GET | Retrieves a cXML application from SignalWire. |
| [List cXML Applications](actions/list-cxml-applications.md) | GET | Retrieves cXML applications from SignalWire. |
| [Update cXML Application](actions/update-cxml-application.md) | PUT | Updates an existing cXML application in SignalWire. |

### C Xml Application Address

| Action | Method | Description |
| --- | --- | --- |
| [List cXML Application Addresses](actions/list-cxml-application-addresses.md) | GET | Retrieves cXML application addresses from SignalWire. |

### C Xml Script

| Action | Method | Description |
| --- | --- | --- |
| [Create cXML Script](actions/create-cxml-script.md) | POST | Creates a new cXML script in SignalWire. |
| [Delete cXML Script](actions/delete-cxml-script.md) | DELETE | Deletes an existing cXML script from SignalWire. |
| [Get cXML Script](actions/get-cxml-script.md) | GET | Retrieves a cXML script from SignalWire. |
| [List cXML Scripts](actions/list-cxml-scripts.md) | GET | Retrieves cXML scripts from SignalWire. |
| [Update cXML Script](actions/update-cxml-script.md) | PUT | Updates an existing cXML script in SignalWire. |

### C Xml Script Address

| Action | Method | Description |
| --- | --- | --- |
| [List cXML Script Addresses](actions/list-cxml-script-addresses.md) | GET | Retrieves cXML script addresses from SignalWire. |

### C Xml Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create cXML Webhook](actions/create-cxml-webhook.md) | POST | Creates a new cXML webhook in SignalWire. |
| [Delete cXML Webhook](actions/delete-cxml-webhook.md) | DELETE | Deletes an existing cXML webhook from SignalWire. |
| [Get cXML Webhook](actions/get-cxml-webhook.md) | GET | Retrieves a cXML webhook from SignalWire. |
| [List cXML Webhooks](actions/list-cxml-webhooks.md) | GET | Retrieves cXML webhooks from SignalWire. |
| [Update cXML Webhook](actions/update-cxml-webhook.md) | PUT | Updates an existing cXML webhook in SignalWire. |

### C Xml Webhook Address

| Action | Method | Description |
| --- | --- | --- |
| [List cXML Webhook Addresses](actions/list-cxml-webhook-addresses.md) | GET | Retrieves cXML webhook addresses from SignalWire. |

### Call Command

| Action | Method | Description |
| --- | --- | --- |
| [Send Call Commands](actions/send-call-commands.md) | PUT | Sends call commands to SignalWire calls. |

### Call Flow

| Action | Method | Description |
| --- | --- | --- |
| [Create Call Flow](actions/create-call-flow.md) | POST | Creates a new call flow in SignalWire. |
| [Delete Call Flow](actions/delete-call-flow.md) | DELETE | Deletes an existing call flow from SignalWire. |
| [Get Call Flow](actions/get-call-flow.md) | GET | Retrieves a call flow from SignalWire. |
| [List Call Flows](actions/list-call-flows.md) | GET | Retrieves call flows from SignalWire. |
| [Update Call Flow](actions/update-call-flow.md) | PUT | Updates an existing call flow in SignalWire. |

### Call Flow Address

| Action | Method | Description |
| --- | --- | --- |
| [List Call Flow Addresses](actions/list-call-flow-addresses.md) | GET | Retrieves call flow addresses from SignalWire. |

### Call Flow Version

| Action | Method | Description |
| --- | --- | --- |
| [Deploy Call Flow Version](actions/deploy-call-flow-version.md) | PUT | Deploys a call flow version in SignalWire. |
| [List Call Flow Versions](actions/list-call-flow-versions.md) | GET | Retrieves call flow versions from SignalWire. |

### Chat Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Token](actions/create-chat-token.md) | POST | Creates a new chat token in SignalWire. |

### Chunk

| Action | Method | Description |
| --- | --- | --- |
| [Delete Chunk](actions/delete-chunk.md) | DELETE | Deletes an existing chunk from SignalWire. |
| [List Chunks](actions/list-chunks.md) | GET | Retrieves chunks from SignalWire. |
| [Retrieve Chunk](actions/retrieve-chunk.md) | GET | Retrieves a chunk from SignalWire. |

### Conference

| Action | Method | Description |
| --- | --- | --- |
| [List Conferences](actions/list-conferences.md) | GET | Retrieves conferences from SignalWire. |

### Conference Room

| Action | Method | Description |
| --- | --- | --- |
| [Create Conference Room](actions/create-conference-room.md) | POST | Creates a new conference room in SignalWire. |
| [Delete Conference Room](actions/delete-conference-room.md) | DELETE | Deletes an existing conference room from SignalWire. |
| [Get Conference Room](actions/get-conference-room.md) | GET | Retrieves a conference room from SignalWire. |
| [List Conference Rooms](actions/list-conference-rooms.md) | GET | Retrieves conference rooms from SignalWire. |
| [Update Conference Room](actions/update-conference-room.md) | PUT | Updates an existing conference room in SignalWire. |

### Conference Room Address

| Action | Method | Description |
| --- | --- | --- |
| [List Conference Room Addresses](actions/list-conference-room-addresses.md) | GET | Retrieves conference room addresses from SignalWire. |

### Dialogflow Agent

| Action | Method | Description |
| --- | --- | --- |
| [Delete Dialogflow Agent](actions/delete-dialogflow-agent.md) | DELETE | Deletes an existing Dialogflow agent from SignalWire. |
| [Get Dialogflow Agent](actions/get-dialogflow-agent.md) | GET | Retrieves a Dialogflow agent from SignalWire. |
| [List Dialogflow Agents](actions/list-dialogflow-agents.md) | GET | Retrieves Dialogflow agents from SignalWire. |
| [Update Dialogflow Agent](actions/update-dialogflow-agent.md) | PUT | Updates an existing Dialogflow agent in SignalWire. |

### Dialogflow Agent Address

| Action | Method | Description |
| --- | --- | --- |
| [List Dialogflow Agent Addresses](actions/list-dialogflow-agent-addresses.md) | GET | Retrieves Dialogflow agent addresses from SignalWire. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create a Document](actions/create-a-document.md) | POST | Creates a new document in SignalWire. |
| [Delete a Document](actions/delete-a-document.md) | DELETE | Deletes an existing document from SignalWire. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from SignalWire. |
| [Update a Document](actions/update-a-document.md) | PUT | Updates an existing document in SignalWire. |

### Embeds Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Guest Embed Token](actions/create-guest-embed-token.md) | POST | Creates a new guest embed token in SignalWire. |

### Exchange A Refresh Token For A New Subscriber Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Refresh Subscriber Token](actions/refresh-subscriber-token.md) | POST | Refreshes a subscriber token in SignalWire. |

### Fabric Addresses Assigned To A Sip Gateway

| Action | Method | Description |
| --- | --- | --- |
| [List Fabric Addresses assigned to a SIP Gateway](actions/list-fabric-addresses-assigned-to-a-sip-gateway.md) | GET | Retrieves Fabric addresses assigned to a SIP gateway from SignalWire. |

### Find A Log By Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Fax Log](actions/get-fax-log.md) | GET | Retrieves a fax log from SignalWire. |
| [Get Message Log](actions/get-message-log.md) | GET | Retrieves a message log from SignalWire. |
| [Get Voice Log](actions/get-voice-log.md) | GET | Retrieves a voice log from SignalWire. |

### Free Switch Connector

| Action | Method | Description |
| --- | --- | --- |
| [Create FreeSWITCH Connector](actions/create-freeswitch-connector.md) | POST | Creates a new FreeSWITCH connector in SignalWire. |
| [Delete FreeSWITCH Connector](actions/delete-freeswitch-connector.md) | DELETE | Deletes an existing FreeSWITCH connector from SignalWire. |
| [Get FreeSWITCH Connector](actions/get-freeswitch-connector.md) | GET | Retrieves a FreeSWITCH connector from SignalWire. |
| [List FreeSWITCH Connectors](actions/list-freeswitch-connectors.md) | GET | Retrieves FreeSWITCH connectors from SignalWire. |
| [Update FreeSWITCH Connector](actions/update-freeswitch-connector.md) | PUT | Updates an existing FreeSWITCH connector in SignalWire. |

### Free Switch Connector Address

| Action | Method | Description |
| --- | --- | --- |
| [List FreeSWITCH Connector Addresses](actions/list-freeswitch-connector-addresses.md) | GET | Retrieves FreeSWITCH connector addresses from SignalWire. |

### Laml Application

| Action | Method | Description |
| --- | --- | --- |
| [Delete cXML Application](actions/delete-cxml-application.md) | DELETE | Deletes an existing cXML application from SignalWire. |

### Log

| Action | Method | Description |
| --- | --- | --- |
| [List Fax Logs](actions/list-fax-logs.md) | GET | Retrieves fax logs from SignalWire. |
| [List Message Logs](actions/list-message-logs.md) | GET | Retrieves message logs from SignalWire. |
| [List Voice Logs](actions/list-voice-logs.md) | GET | Retrieves voice logs from SignalWire. |

### Log Event

| Action | Method | Description |
| --- | --- | --- |
| [List Log Events](actions/list-log-events.md) | GET | Retrieves voice log events from SignalWire. |

### Pub Sub Token

| Action | Method | Description |
| --- | --- | --- |
| [Create PubSub Token](actions/create-pubsub-token.md) | POST | Creates a new PubSub token in SignalWire. |

### Relay Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Relay Application](actions/create-relay-application.md) | POST | Creates a new relay application in SignalWire. |
| [Delete Relay Application](actions/delete-relay-application.md) | DELETE | Deletes an existing relay application from SignalWire. |
| [Get Relay Application](actions/get-relay-application.md) | GET | Retrieves a relay application from SignalWire. |
| [List Relay Applications](actions/list-relay-applications.md) | GET | Retrieves relay applications from SignalWire. |
| [Update Relay Application](actions/update-relay-application.md) | PUT | Updates an existing relay application in SignalWire. |

### Relay Application Address

| Action | Method | Description |
| --- | --- | --- |
| [List Relay Application Addresses](actions/list-relay-application-addresses.md) | GET | Retrieves relay application addresses from SignalWire. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Delete Resource](actions/delete-resource.md) | DELETE | Deletes an existing resource from SignalWire. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from SignalWire. |
| [List Fabric Resources](actions/list-fabric-resources.md) | GET | Retrieves Fabric resources from SignalWire. |

### Resource Address

| Action | Method | Description |
| --- | --- | --- |
| [List Resource Addresses](actions/list-resource-addresses.md) | GET | Retrieves resource addresses from SignalWire. |

### Search Document

| Action | Method | Description |
| --- | --- | --- |
| [Search Documents](actions/search-documents.md) | GET | Searches documents in SignalWire by query string. |

### Sip Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create SIP Endpoint](actions/create-sip-endpoint.md) | POST | Creates a new SIP endpoint in SignalWire. |
| [Delete SIP Endpoint](actions/delete-sip-endpoint.md) | DELETE | Deletes an existing SIP endpoint from SignalWire. |
| [Get SIP Endpoint](actions/get-sip-endpoint.md) | GET | Retrieves a SIP endpoint from SignalWire. |
| [List SIP Endpoints](actions/list-sip-endpoints.md) | GET | Retrieves SIP endpoints from SignalWire. |
| [Update SIP Endpoint](actions/update-sip-endpoint.md) | PUT | Updates an existing SIP endpoint in SignalWire. |

### Sip Endpoint Address

| Action | Method | Description |
| --- | --- | --- |
| [List SIP Endpoint Addresses](actions/list-sip-endpoint-addresses.md) | GET | Retrieves SIP endpoint addresses from SignalWire. |

### Sip Gateway

| Action | Method | Description |
| --- | --- | --- |
| [Create SIP Gateway](actions/create-sip-gateway.md) | POST | Creates a new SIP gateway in SignalWire. |
| [Delete SIP Gateway](actions/delete-sip-gateway.md) | DELETE | Deletes an existing SIP gateway from SignalWire. |
| [Get SIP Gateway](actions/get-sip-gateway.md) | GET | Retrieves a SIP gateway from SignalWire. |
| [List SIP Gateways](actions/list-sip-gateways.md) | GET | Retrieves SIP gateways from SignalWire. |
| [Update SIP Gateway](actions/update-sip-gateway.md) | PUT | Updates an existing SIP gateway in SignalWire. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in SignalWire. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from SignalWire. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from SignalWire. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from SignalWire. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in SignalWire. |

### Subscriber Address

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriber Addresses](actions/list-subscriber-addresses.md) | GET | Retrieves subscriber addresses from SignalWire. |

### Subscriber Guest Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber Guest Token](actions/create-subscriber-guest-token.md) | POST | Creates a new subscriber guest token in SignalWire. |

### Subscriber Invite Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber Invite Token](actions/create-subscriber-invite-token.md) | POST | Creates a new subscriber invite token in SignalWire. |

### Subscriber Sip Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber SIP Endpoint](actions/create-subscriber-sip-endpoint.md) | POST | Creates a new subscriber SIP endpoint in SignalWire. |
| [Delete Subscriber SIP Endpoint](actions/delete-subscriber-sip-endpoint.md) | DELETE | Deletes an existing subscriber SIP endpoint from SignalWire. |
| [Get Subscriber SIP Endpoint](actions/get-subscriber-sip-endpoint.md) | GET | Retrieves a subscriber SIP endpoint from SignalWire. |
| [List Subscriber SIP Endpoints](actions/list-subscriber-sip-endpoints.md) | GET | Retrieves subscriber SIP endpoints from SignalWire. |
| [Update Subscriber SIP Endpoint](actions/update-subscriber-sip-endpoint.md) | PUT | Updates an existing subscriber SIP endpoint in SignalWire. |

### Subscriber Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber Token](actions/create-subscriber-token.md) | POST | Creates a new subscriber token in SignalWire. |

### Swml Script

| Action | Method | Description |
| --- | --- | --- |
| [Create SWML Script](actions/create-swml-script.md) | POST | Creates a new SWML script in SignalWire. |
| [Delete SWML Script](actions/delete-swml-script.md) | DELETE | Deletes an existing SWML script from SignalWire. |
| [Get SWML Script](actions/get-swml-script.md) | GET | Retrieves a SWML script from SignalWire. |
| [List SWML Scripts](actions/list-swml-scripts.md) | GET | Retrieves SWML scripts from SignalWire. |
| [Update SWML Script](actions/update-swml-script.md) | PUT | Updates an existing SWML script in SignalWire. |

### Swml Script Address

| Action | Method | Description |
| --- | --- | --- |
| [List SWML Script Addresses](actions/list-swml-script-addresses.md) | GET | Retrieves SWML script addresses from SignalWire. |

### Swml Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create SWML Webhook](actions/create-swml-webhook.md) | POST | Creates a new SWML webhook in SignalWire. |
| [Delete SWML Webhook](actions/delete-swml-webhook.md) | DELETE | Deletes an existing SWML webhook from SignalWire. |
| [Get SWML Webhook](actions/get-swml-webhook.md) | GET | Retrieves a SWML webhook from SignalWire. |
| [List SWML Webhooks](actions/list-swml-webhooks.md) | GET | Retrieves SWML webhooks from SignalWire. |
| [Update SWML Webhook](actions/update-swml-webhook.md) | PUT | Updates an existing SWML webhook in SignalWire. |

### Swml Webhook Address

| Action | Method | Description |
| --- | --- | --- |
| [List SWML Webhook Addresses](actions/list-swml-webhook-addresses.md) | GET | Retrieves SWML webhook addresses from SignalWire. |

