# Process a âDoc with Veryfi

Creates a new AnyDoc in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/any-documents`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Process a âDoc](https://docs.veryfi.com/api/anydocs/process-a-A-doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `meta.tags[]` | body | `array<string>` | no | Possible values: non-empty Default value: `` Tags you want to associate with the document. |
| `package_path` | body | `string` | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `file_data` | body | `string` | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `file_url` | body | `string` | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file_name` | body | `string` | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `max_pages_to_process` | body | `number` | no | Possible values: >= 1 and <= 50 Default value: 20 The number of pages to process for the document. The limit is 50 pages per document. |
| `blueprint_name` | body | `string` | no | Possible values: non-empty The name of the extraction blueprints. Default blueprints include [auto_insurance_card, bill_of_lading, flight_itinerary, goods_received_note, incorporation_document, incorporation_document_latam, indian_passport, latam_passport, prescription_medication_label, product_nutrition_facts, restaurant_menu, shipping_label, uk_drivers_license, us_driver_license, us_health_insurance_card, us_passport, vehicle_registration, vendor_statement, work_order] |
| `template_name` | body | `string` | no | Possible values: non-empty Deprecated.The blueprint name which was used to extract the data. Same as blueprint_name. |
| `meta.external_id` | body | `string` | no | Possible values: non-empty External ID you want to associate with the document. |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
