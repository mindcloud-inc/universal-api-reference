# Process a Document with Veryfi

Creates a new document in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/documents`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Process a Document](https://docs.veryfi.com/api/receipts-invoices/process-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | no | A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `package_path` | body | `string` | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `file_data` | body | `string` | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `file_url` | body | `string` | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file_name` | body | `string` | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `bounding_boxes` | body | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | body | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `detailed` | body | `boolean` | no | This field was deprecated on 2023-08-20. Use bounding_boxes and confidence_details . |
| `categories[]` | body | `array<string>` | no | Possible values: non-empty Default value: `` A list of custom categories . Veryfi will match the document and line items with the specified categories. Does not work with the parameter boost_mode set to true . |
| `tags[]` | body | `array<string>` | no | Possible values: non-empty Default value: `` A user-defined list of identifiers that help to categorize or flag particular types of documents. The Document object can have multiple tags. You can create tags by API or in Hub . |
| `max_pages_to_process` | body | `number` | no | The number of pages to process for the document. The default limit is 15 pages per document. |
| `boost_mode` | body | `boolean` | no | Default value: false A parameter indicating whether or not boost mode should be enabled. Boost mode skips data enrichment steps allowing for faster processing time. The default value for boost_mode is false . |
| `async` | body | `boolean` | no | Default value: false A parameter used to process files asynchronously using webhooks . Set async to true to use async mode . The default value is false . |
| `detect_blur` | body | `boolean` | no | Default value: false A parameter used to determine whether or not the uploaded document is blurry or not. This field is deprecated, use meta.pages.is_blurry . |
| `parse_address` | body | `boolean` | no | Default value: false A parameter used to determine whether or not to break an address into its individual components. This adds parsed_address to the response object. |
| `crop_document` | body | `boolean` | no | A parameter used to determine whether or not disable document cropping. Cropping is on by default |
| `compute` | body | `boolean` | no | Default value: true A parameter used to determine whether or not to include enrichments on several fields to provide high extraction coverage when the data is not present or extracted from the document. The default value is true . |
| `country` | body | `string` | no | Possible values: [ GR , NU , SR , GH , BJ , SA , KN , JO , NZ , AO , JP , ID , LV , OM , SB , HU , BN , SK , LI , SM , AN , AE , IQ , MG , RO , ZW , KY , UG , CA , NF , TN , GG , TG , KG , LY , PA , BO , KM , BS , GE , QA , NI , MW , CL , GU , VN , NO , AG , BL , PR , SZ , AT , DE , IL , FM , UM , LR , KH , KW , LC , TC , LB , BR , CV , LA , VU , CR , IR , SC , LS , GQ , ST , CX , IO , BM , ML , PM , TK , LT , PF , ME , MQ , MA , FJ , PG , KI , PH , SJ , BV , DZ , CK , PY , HT , VG , EC , SH , CF , CG , GI , DO , HN , GY , BI , AM , KP , MX , NC , AU , SV , CI , GF , NE , WS , TF , MF , SG , WF , CC , BH , DK , IN , CD , GM , MV , MZ , GW , TH , AW , VC , YE , GS , BF , MO , MM , CH , VA , ET , SY , PK , RW , TW , LK , CY , SL , BG , IT , JE , AD , NR , TZ , RS , TJ , GB , UZ , AI , ZA , MY , BZ , MD , RU , CZ , ER , HK , VE , AX , IE , ZM , NL , BD , RE , SD , BB , EH , AS , CN , MC , JM , FO , FR , MP , SI , BW , DJ , US , BE , KZ , PS , GD , AR , GP , TD , AZ , NP , TL , GT , BY , VI , MR , EE , CM , HM , MH , KR , GL , SN , PL , DM , CU , PT , IS , AF , BT , MT , GN , CO , KE , MN , SE , MK , MS , TT , UY , AL , PE , UA , LU , HR , PW , TR , EG , TO , YT , TM , IM , PN , ES , TV , AQ , NA , MU , BA , FK , GA , NG , FI , SO ] A parameter used to provide an additional hint to help the model recognize the currency of the document. |
| `emailed_receipt_id` | body | `number` | no | — |
| `receipt_id` | body | `number` | no | — |
| `document_type` | body | `string` | no | Possible values: [ check , credit_note , invoice , long_receipt , other , purchase_order , receipt , statement , w8 , w9 , remittance_advice , contract ] |
| `auto_delete` | body | `boolean` | no | Delete this document from Veryfi after data has been extracted |
| `device_data` | body | `string` | no | Device data vocab to help with fraudulent data Device unique identifier string string Browser identifying characteristics Manually defined source Unique user identifier, like a digital fingerprint (hashed login) used to access the app where they upload their documents. Used in fraud detection. string string Any request, device or document metadata to store, like uploading speed, etc. Possible values: >= 0.001 and <= 1800 Uploading time in seconds |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
