# Blueink: Native API Reference

A consolidated summary of Blueink's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.blueink.com/docs/
- **OpenAPI specification:** https://developer.blueink.com/redocusaurus/blueink-api-v2.yaml
- **API base URL:** `https://api.blueink.com/api/v2`

## Authentication

### API Key

Authenticate Blueink API requests with a private API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.blueink.com/docs/esignature-api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Bundle Tags](actions/add-bundle-tags.md) | `PUT /bundles/:bundleSlug/add_tags/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/addBundleTags) |
| [Cancel Bundle](actions/cancel-bundle.md) | `PUT /bundles/:bundleSlug/cancel/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/cancelBundle) |
| [Create Bundle](actions/create-bundle.md) | `POST /bundles/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/createBundle) |
| [Create Bundle from Envelope Template](actions/create-bundle-from-envelope-template.md) | `POST /bundles/create_from_envelope_template/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/createBundleFromEnvelopeTemplate) |
| [Create Embedded Signing URL](actions/create-embedded-signing-url.md) | `POST /packets/:packetId/embed_url/` | [docs](https://developer.blueink.com/api/#tag/Packet/operation/createPacketEmbedURL) |
| [Create Person](actions/create-person.md) | `POST /persons/` | [docs](https://developer.blueink.com/api/#tag/Person/operation/createPerson) |
| [Delete Person](actions/delete-person.md) | `DELETE /persons/:personId/` | [docs](https://developer.blueink.com/api/#tag/Person/operation/deletePerson) |
| [List Bundle Events](actions/list-bundle-events.md) | `GET /bundles/:bundleSlug/events/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/listBundleEvents) |
| [List Bundles](actions/list-bundles.md) | `GET /bundles/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/listBundles) |
| [List Document Templates](actions/list-document-templates.md) | `GET /templates/` | [docs](https://developer.blueink.com/api/#tag/Templates/operation/listTemplates) |
| [List Envelope Templates](actions/list-envelope-templates.md) | `GET /envelope-templates/` | [docs](https://developer.blueink.com/api/#tag/Envelope-Templates/operation/listEnvelopeTemplates) |
| [List Persons](actions/list-persons.md) | `GET /persons/` | [docs](https://developer.blueink.com/api/#tag/Person/operation/listPersons) |
| [Remove Bundle Tags](actions/remove-bundle-tags.md) | `PUT /bundles/:bundleSlug/remove_tags/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/removeBundleTags) |
| [Retrieve Bundle](actions/retrieve-bundle.md) | `GET /bundles/:bundleSlug/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/retrieveBundle) |
| [Retrieve Bundle Data](actions/retrieve-bundle-data.md) | `GET /bundles/:bundleSlug/data/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/getBundleData) |
| [Retrieve Bundle Files](actions/retrieve-bundle-files.md) | `GET /bundles/:bundleSlug/files/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/getBundleFiles) |
| [Retrieve Document Template](actions/retrieve-document-template.md) | `GET /templates/:templateId/` | [docs](https://developer.blueink.com/api/#tag/Templates/operation/retrieveTemplate) |
| [Retrieve Packet](actions/retrieve-packet.md) | `GET /packets/:packetId/` | [docs](https://developer.blueink.com/api/#tag/Packet/operation/retrievePacket) |
| [Retrieve Packet Certificate of Evidence](actions/retrieve-packet-certificate-of-evidence.md) | `GET /packets/:packetId/coe/` | [docs](https://developer.blueink.com/api/#tag/Packet/operation/getPacketCOE) |
| [Retrieve Person](actions/retrieve-person.md) | `GET /persons/:personId/` | [docs](https://developer.blueink.com/api/#tag/Person/operation/getPerson) |
| [Send Reminder](actions/send-packet-reminder.md) | `PUT /packets/:packetId/remind/` | [docs](https://developer.blueink.com/api/#tag/Packet/operation/sendPacketReminder) |
| [Update Bundle](actions/update-bundle.md) | `PATCH /bundles/:bundleSlug/` | [docs](https://developer.blueink.com/api/#tag/Bundles/operation/updateBundlePartial) |
| [Update Packet](actions/update-packet.md) | `PATCH /packets/:packetId/` | [docs](https://developer.blueink.com/api/#tag/Packet/operation/updatePacket) |
| [Update Person](actions/update-person.md) | `PUT /persons/:personId/` | [docs](https://developer.blueink.com/api/#tag/Person/operation/updatePerson) |
