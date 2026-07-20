# Create Offer with Recruitee ATS

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/offers`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Create Offer](https://docs.recruitee.com/reference/offersid-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offer.title` | body | `string` | yes | Offer title. |
| `offer.kind` | body | `string` | no | Offer kind. |
| `offer.location_ids` | body | `list<number>` | yes | Offer location IDs. |
| `offer.description` | body | `string` | yes | Offer description. |
| `offer.requirements` | body | `string` | yes | Offer requirements. |
| `offer.department_id` | body | `number` | no | Department ID. |
| `offer.on_site` | body | `boolean` | no | Whether the offer is on-site. |
| `offer.hybrid` | body | `boolean` | no | Whether the offer is hybrid. |
| `offer.remote` | body | `boolean` | no | Whether the offer is remote. |
| `offer.visibility_options` | body | `list<string>` | no | Visibility options for the offer. |
| `offer.locations_question` | body | `string` | no | Location picker question text. |
| `offer.locations_question_type` | body | `string` | no | Location question type. |
| `offer.locations_question_required` | body | `boolean` | no | Whether the location question is required. |
