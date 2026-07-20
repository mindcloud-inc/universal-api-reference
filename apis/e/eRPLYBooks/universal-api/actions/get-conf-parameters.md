# ERPLY Books: Get Configuration Parameters

Retrieves configuration parameters from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-conf-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-conf-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-conf-parameters?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "account_links": {
            "help": "https://example.com",
            "helpPOS": "https://example.com",
            "knowledge_base": "https://example.com",
            "terms_of_service": "https://example.com"
          },
          "account_stats_updated": "string",
          "accounts_receivable_listed": "string",
          "actual_reports_username": "Ava Chen",
          "additionalModules": [
            {
              "enabled": 1,
              "name": "Ava Chen"
            }
          ],
          "allow_partial_fulfilment_in_report": "string",
          "api_getpointsofsale_all_invoice_numbers_not_returned": "string",
          "app_interface": "string",
          "assortments_rights_initialized": "string",
          "billing_invoice_use_todays_date": "string",
          "branding": "string",
          "change_pos_version_rights_initialized": "string",
          "code_on_invoice": "string",
          "country": "string",
          "credit_payments_are_created_correctly": "string",
          "csv_field_separator": "string",
          "customer_manager_rights_updated": "string",
          "date_installed": "string",
          "dateformat": "string",
          "default_client_idDat": "string",
          "default_currency": "string",
          "default_language": "string",
          "default_price_decimals": "string",
          "discount_printed_on_invoices": "string",
          "do_not_show_discounts_on_customer_card": "string",
          "employee_identifier_on_receipt": "string",
          "employee_identifier_on_sales_document": "string",
          "enable_automatic_version_upgrade": "string",
          "enable_delivery_date_tracking": "string",
          "erply_news_dashboard": "string",
          "final_price_input_on_invoice": "string",
          "full_image_dir": "string",
          "go_date_format": "string",
          "go_date_time_format": "string",
          "go_hour_minute_format": "string",
          "go_month_day_format": "string",
          "go_time_format": "string",
          "googleapps_default_usergroup": "string",
          "inventory_modules_rights_updated": "string",
          "inventory_reports_rights_updated": "string",
          "invoice_algorithm_version": 1,
          "invoice_client_is_payer": "string",
          "invoice_payer_indexed": "string",
          "invoice_print_rows1p": "string",
          "invoice_print_rowsNp": "string",
          "invoice_rounding": "string",
          "invoice_waybills_show_price_with_tax": 1,
          "jsplugin_appstore_enabled": "string",
          "jsplugin_cdn_enabled": "string",
          "jsplugin_cdn_pictures_uploader_enabled": "string",
          "jsplugin_import_enabled": "string",
          "jsplugin_stocktakings_enabled": "string",
          "jsplugin_woocommerce_enabled": "string",
          "langs": "string",
          "languages": "string",
          "locale_uses_price_with_tax": 1,
          "make_sales_reports_by_revenue": "string",
          "mask_email_addresses_in_log": "ava@example.com",
          "matrix_update_code": "string",
          "matrix_update_commission_amount": "string",
          "matrix_update_costprice": "string",
          "matrix_update_isactive": "string",
          "matrix_update_name": "Ava Chen",
          "matrix_update_price": "string",
          "matrix_update_show_in_webshop": "string",
          "matrix_update_variations_automatically": "string",
          "my_company_info_rights_initialized": "string",
          "new_inventory_start_date": "string",
          "numberformat": "string",
          "org_idDat": "string",
          "parameter_sets_rights_initialized": "string",
          "partial_fulfilment_splits_order": "string",
          "payment_info_in_table": "string",
          "pos_allow_sale_giftcard_regular": "string",
          "pos_allow_sale_giftcard_serial": "string",
          "pos_opening_required": "string",
          "pos_version_1_disabled": "string",
          "pos_version_pos2020_disabled": "string",
          "pos_version_touch_disabled": "string",
          "pos_version_web_disabled": "string",
          "prcorder_status_when_partially_received": "string",
          "prcorders_enable_partial_fulfilling": "string",
          "price_decimals": 1,
          "pricelist_zero_price_algorithm_updated": "string",
          "print_customer_regcode_on_invoice": "string",
          "print_giftcard_balance_on_receipt": "string",
          "product_code_unique": "string",
          "product_code2_unique": "string",
          "product_families_rights_initialized": "string",
          "product_names_editable_on_invoice": "Ava Chen",
          "promotion_tiers_rights_initialized": "string",
          "purchase_order_canceled_status_id": "string",
          "purchase_orders_rights_initialized": "string",
          "quickbooks_include_same_day_invoices_and_payments": "string",
          "ref_no": "string",
          "report_generator_rights_updated": "string",
          "reserved_product_lookup_uses_virtual_columns": "string",
          "reward_points_is_double": "string",
          "send_emails_from_company_address": "ava@example.com",
          "services_disabled": "string",
          "show_price_with_vat": "string",
          "show_row_currency_on_invoice": "string",
          "store_manager_settings_rights_initialized": "string",
          "storecredit_enabled_on_salepoint_card": "string",
          "tablesize_user": "string",
          "tablesize_user_updated": "string",
          "thumb_image_dir": "string",
          "thumb_use": "string",
          "thumb_x": "string",
          "thumb_y": "string",
          "timezone": "string",
          "touchpos_disable_external_card_payment": "string",
          "touchpos_disable_product_row_auto_open": "string",
          "touchscreen_pos": "string",
          "touchscreen_pos_version": "string",
          "unconfirmed_document_permissions_initialized": "string",
          "unconfirmed_document_rights_initialized": "string",
          "unpaid_invoices_reports_rights_updated": "string",
          "use_attendants_in_pos": "string",
          "use_ems_service": "string",
          "use_inv_inv_table": "string",
          "use_m2_calculator": "string",
          "use_menu_component": "string",
          "use_prcinv_prcinv_table": "string",
          "use_transport_costs": "string",
          "users_can_only_see_own_warehouse_stock": "string",
          "users_can_see_only_own_warehouse_documents": "string",
          "vat_number_always_on_invoice": "string",
          "vertical": "string",
          "view_image_dir": "string",
          "view_use": "string",
          "view_x": "string",
          "view_y": "string",
          "warehouse_fixed2": "string",
          "web_image_dir": "string",
          "web_use": "string",
          "web_x": "string",
          "web_y": "string",
          "zreport_hide_drawer_openings": "string"
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].account_links.help` | string |  |
| `records[].account_links.helpPOS` | string |  |
| `records[].account_links.knowledge_base` | string |  |
| `records[].account_links.terms_of_service` | string |  |
| `records[].account_stats_updated` | string |  |
| `records[].accounts_receivable_listed` | string |  |
| `records[].actual_reports_username` | string |  |
| `records[].additionalModules[].enabled` | number |  |
| `records[].additionalModules[].name` | string |  |
| `records[].allow_partial_fulfilment_in_report` | string |  |
| `records[].api_getpointsofsale_all_invoice_numbers_not_returned` | string |  |
| `records[].app_interface` | string |  |
| `records[].assortments_rights_initialized` | string |  |
| `records[].billing_invoice_use_todays_date` | string |  |
| `records[].branding` | string |  |
| `records[].change_pos_version_rights_initialized` | string |  |
| `records[].code_on_invoice` | string |  |
| `records[].country` | string |  |
| `records[].credit_payments_are_created_correctly` | string |  |
| `records[].csv_field_separator` | string |  |
| `records[].customer_manager_rights_updated` | string |  |
| `records[].date_installed` | string |  |
| `records[].dateformat` | string |  |
| `records[].default_client_idDat` | string |  |
| `records[].default_currency` | string |  |
| `records[].default_language` | string |  |
| `records[].default_price_decimals` | string |  |
| `records[].discount_printed_on_invoices` | string |  |
| `records[].do_not_show_discounts_on_customer_card` | string |  |
| `records[].employee_identifier_on_receipt` | string |  |
| `records[].employee_identifier_on_sales_document` | string |  |
| `records[].enable_automatic_version_upgrade` | string |  |
| `records[].enable_delivery_date_tracking` | string |  |
| `records[].erply_news_dashboard` | string |  |
| `records[].final_price_input_on_invoice` | string |  |
| `records[].full_image_dir` | string |  |
| `records[].go_date_format` | string |  |
| `records[].go_date_time_format` | string |  |
| `records[].go_hour_minute_format` | string |  |
| `records[].go_month_day_format` | string |  |
| `records[].go_time_format` | string |  |
| `records[].googleapps_default_usergroup` | string |  |
| `records[].inventory_modules_rights_updated` | string |  |
| `records[].inventory_reports_rights_updated` | string |  |
| `records[].invoice_algorithm_version` | number |  |
| `records[].invoice_client_is_payer` | string |  |
| `records[].invoice_payer_indexed` | string |  |
| `records[].invoice_print_rows1p` | string |  |
| `records[].invoice_print_rowsNp` | string |  |
| `records[].invoice_rounding` | string |  |
| `records[].invoice_waybills_show_price_with_tax` | number |  |
| `records[].jsplugin_appstore_enabled` | string |  |
| `records[].jsplugin_cdn_enabled` | string |  |
| `records[].jsplugin_cdn_pictures_uploader_enabled` | string |  |
| `records[].jsplugin_import_enabled` | string |  |
| `records[].jsplugin_stocktakings_enabled` | string |  |
| `records[].jsplugin_woocommerce_enabled` | string |  |
| `records[].langs` | string |  |
| `records[].languages` | string |  |
| `records[].locale_uses_price_with_tax` | number |  |
| `records[].make_sales_reports_by_revenue` | string |  |
| `records[].mask_email_addresses_in_log` | string |  |
| `records[].matrix_update_code` | string |  |
| `records[].matrix_update_commission_amount` | string |  |
| `records[].matrix_update_costprice` | string |  |
| `records[].matrix_update_isactive` | string |  |
| `records[].matrix_update_name` | string |  |
| `records[].matrix_update_price` | string |  |
| `records[].matrix_update_show_in_webshop` | string |  |
| `records[].matrix_update_variations_automatically` | string |  |
| `records[].my_company_info_rights_initialized` | string |  |
| `records[].new_inventory_start_date` | string |  |
| `records[].numberformat` | string |  |
| `records[].org_idDat` | string |  |
| `records[].parameter_sets_rights_initialized` | string |  |
| `records[].partial_fulfilment_splits_order` | string |  |
| `records[].payment_info_in_table` | string |  |
| `records[].pos_allow_sale_giftcard_regular` | string |  |
| `records[].pos_allow_sale_giftcard_serial` | string |  |
| `records[].pos_opening_required` | string |  |
| `records[].pos_version_1_disabled` | string |  |
| `records[].pos_version_pos2020_disabled` | string |  |
| `records[].pos_version_touch_disabled` | string |  |
| `records[].pos_version_web_disabled` | string |  |
| `records[].prcorder_status_when_partially_received` | string |  |
| `records[].prcorders_enable_partial_fulfilling` | string |  |
| `records[].price_decimals` | number |  |
| `records[].pricelist_zero_price_algorithm_updated` | string |  |
| `records[].print_customer_regcode_on_invoice` | string |  |
| `records[].print_giftcard_balance_on_receipt` | string |  |
| `records[].product_code_unique` | string |  |
| `records[].product_code2_unique` | string |  |
| `records[].product_families_rights_initialized` | string |  |
| `records[].product_names_editable_on_invoice` | string |  |
| `records[].promotion_tiers_rights_initialized` | string |  |
| `records[].purchase_order_canceled_status_id` | string |  |
| `records[].purchase_orders_rights_initialized` | string |  |
| `records[].quickbooks_include_same_day_invoices_and_payments` | string |  |
| `records[].ref_no` | string |  |
| `records[].report_generator_rights_updated` | string |  |
| `records[].reserved_product_lookup_uses_virtual_columns` | string |  |
| `records[].reward_points_is_double` | string |  |
| `records[].send_emails_from_company_address` | string |  |
| `records[].services_disabled` | string |  |
| `records[].show_price_with_vat` | string |  |
| `records[].show_row_currency_on_invoice` | string |  |
| `records[].store_manager_settings_rights_initialized` | string |  |
| `records[].storecredit_enabled_on_salepoint_card` | string |  |
| `records[].tablesize_user` | string |  |
| `records[].tablesize_user_updated` | string |  |
| `records[].thumb_image_dir` | string |  |
| `records[].thumb_use` | string |  |
| `records[].thumb_x` | string |  |
| `records[].thumb_y` | string |  |
| `records[].timezone` | string |  |
| `records[].touchpos_disable_external_card_payment` | string |  |
| `records[].touchpos_disable_product_row_auto_open` | string |  |
| `records[].touchscreen_pos` | string |  |
| `records[].touchscreen_pos_version` | string |  |
| `records[].unconfirmed_document_permissions_initialized` | string |  |
| `records[].unconfirmed_document_rights_initialized` | string |  |
| `records[].unpaid_invoices_reports_rights_updated` | string |  |
| `records[].use_attendants_in_pos` | string |  |
| `records[].use_ems_service` | string |  |
| `records[].use_inv_inv_table` | string |  |
| `records[].use_m2_calculator` | string |  |
| `records[].use_menu_component` | string |  |
| `records[].use_prcinv_prcinv_table` | string |  |
| `records[].use_transport_costs` | string |  |
| `records[].users_can_only_see_own_warehouse_stock` | string |  |
| `records[].users_can_see_only_own_warehouse_documents` | string |  |
| `records[].vat_number_always_on_invoice` | string |  |
| `records[].vertical` | string |  |
| `records[].view_image_dir` | string |  |
| `records[].view_use` | string |  |
| `records[].view_x` | string |  |
| `records[].view_y` | string |  |
| `records[].warehouse_fixed2` | string |  |
| `records[].web_image_dir` | string |  |
| `records[].web_use` | string |  |
| `records[].web_x` | string |  |
| `records[].web_y` | string |  |
| `records[].zreport_hide_drawer_openings` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conf-parameters.md) for the provider-specific parameters and requirements.

