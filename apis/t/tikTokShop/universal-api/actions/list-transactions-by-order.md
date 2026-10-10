# TikTok Shop: List Transactions by Order



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/list-transactions-by-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/list-transactions-by-order?connectionId=$CONNECTION_ID&orderId=string&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string",
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/list-transactions-by-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes |  |
| `shopCipher` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "feeAndTaxAmount": "string",
      "orderCreateTime": 1,
      "orderId": "string",
      "revenueAmount": "string",
      "settlementAmount": "string",
      "shippingCostAmount": "string",
      "skuTransactions": [
        {
          "feeTaxAmount": "string",
          "feeTaxBreakdown": {
            "fee": {
              "affiliateAdsCommissionAmount": "string",
              "affiliateCommissionAmount": "string",
              "affiliateCommissionAmountBeforePit": "string",
              "affiliateCommissionDeposit": "string",
              "affiliateCommissionRelease": "string",
              "affiliatePartnerCommissionAmount": "string",
              "autoPostShoppableVideoCommissionFee": "string",
              "bonusCashbackServiceFeeAmount": "string",
              "brandAmplificationProgramCommission": "string",
              "brandAmplificationProgramFeeTax": "string",
              "brandCampaignFee": "string",
              "brandCampaignFeeTax": "string",
              "buyerFaultReturnShippingFee": "string",
              "campaignPeriodFeeCfpAmount": "string",
              "campaignPeriodFeeCfpTaxAmount": "string",
              "campaignPeriodFeeSpAmount": "string",
              "campaignPeriodFeeSpTaxAmount": "string",
              "categoryLedCampaignFeeAmount": "string",
              "categoryLedCampaignFeeTaxAmount": "string",
              "cofundedCreatorBonusAmount": "string",
              "cofundedPromotionServiceFeeAmount": "string",
              "cpsShopAdsCommissionTaxAmount": "string",
              "creditCardHandlingFeeAmount": "string",
              "dtHandlingFeeAmount": "string",
              "dynamicCommissionAmount": "string",
              "eprPobServiceFeeAmount": "string",
              "externalAffiliateMarketingFeeAmount": "string",
              "failedDeliveryShippingFee": "string",
              "feePerItemSoldAmount": "string",
              "flashSalesServiceFeeAmount": "string",
              "gmvMaxAdFeeAmount": "string",
              "gmvMaxCouponFee": "string",
              "installationServiceFee": "string",
              "insuranceFee": "string",
              "liveSpecialsFeeAmount": "string",
              "mallServiceFeeAmount": "string",
              "newCustomerGrowthPackageFee": "string",
              "platformCommissionAmount": "string",
              "platformSemiManagedCommissionFee": "string",
              "platformSemiManagedCommissionFeeTax": "string",
              "platformSpecialServiceFeeAmount": "string",
              "preOrderServiceFeeAmount": "string",
              "referralFeeAmount": "string",
              "refundAdministrationFeeAmount": "string",
              "sellerGrowthFeeAmount": "string",
              "sellerPaylaterHandlingFeeAmount": "string",
              "sfpServiceFeeAmount": "string",
              "shippingFeeGuaranteeServiceFee": "string",
              "shippingInsuranceFeeTaxAmount": "string",
              "smartPromotionFeeAmount": "string",
              "storeGmvGrowthPackageFee": "string",
              "tapShopAdsCommission": "string",
              "targetProductGmvGrowthPackageFee": "string",
              "transactionFeeAmount": "string",
              "tspCommissionAmount": "string",
              "vnFixInfrastructureFee": "string",
              "voucherXtraServiceFeeAmount": "string"
            },
            "tax": {
              "antiDumpingDutyAmount": "string",
              "article22IncomeTaxWithheld": "string",
              "autoPostShoppableVideoSalesTax": "string",
              "cedularTax": "string",
              "customsClearanceAmount": "string",
              "customsDutyAmount": "string",
              "gstAmount": "string",
              "importVatAmount": "string",
              "isrAmount": "string",
              "ivaAmount": "string",
              "newCustomerGrowthPackageFeeTax": "string",
              "pitAmount": "string",
              "salesTaxReferralFeeAmount": "string",
              "smartPromotionFeeTaxAmount": "string",
              "sstAmount": "string",
              "storeGmvGrowthPackageFeeSalesTax": "string",
              "targetProductGmvGrowthPackageTax": "string",
              "vatAmount": "string"
            }
          },
          "productName": "Ava Chen",
          "quantity": "string",
          "revenueAmount": "string",
          "revenueBreakdown": {
            "codServiceFeeAmount": "string",
            "distantItemFeeAmount": "string",
            "refundCodServiceFeeAmount": "string",
            "refundSubtotalBeforeDiscountAmount": "string",
            "sellerDiscountAmount": "string",
            "sellerDiscountRefundAmount": "string",
            "subtotalBeforeDiscountAmount": "string"
          },
          "settlementAmount": "string",
          "shippingCostAmount": "string",
          "shippingCostBreakdown": {
            "actualShippingFeeAmount": "string",
            "customerPaidShippingFeeAmount": "string",
            "distantShippingFeeAmount": "string",
            "exchangeShippingFeeAmount": "string",
            "failedDeliverySubsidyAmount": "string",
            "fbtFreeShippingFeeAmount": "string",
            "fbtFulfillmentFeeReimbursementAmount": "string",
            "fbtKeyMerchantSubsidy": "string",
            "fbtOverallMerchantSubsidy": "string",
            "freeReturnSubsidyAmount": "string",
            "hazmatHandlingFee": "string",
            "hazmatNoncomplianceFee": "string",
            "internationalLegLogisticsAmount": "string",
            "logisticsServiceFee": "string",
            "nonStandardDimensionFee": "string",
            "nonStandardWeightFee": "string",
            "replacementShippingFeeAmount": "string",
            "returnShippingFeeAmount": "string",
            "returnShippingFeePaidBuyerAmount": "string",
            "returnShippingLabelFeeAmount": "string",
            "sellerSelfShippingServiceFeeAmount": "string",
            "shippingAppServiceFeeAmount": "string",
            "shippingFeeDiscountAmount": "string",
            "shippingInsuranceFeeAmount": "string",
            "signatureConfirmationFeeAmount": "string",
            "supplementaryComponent": {
              "customerShippingFeeOffsetAmount": "string",
              "fbmShippingCostAmount": "string",
              "fbtFulfillmentFeeAmount": "string",
              "fbtShippingCostAmount": "string",
              "platformShippingFeeDiscountAmount": "string",
              "promoShippingIncentiveAmount": "string",
              "refundedCustomerShippingFeeAmount": "string",
              "returnRefundSubsidyAmount": "string",
              "sellerShippingFeeDiscountAmount": "string",
              "shippingFeeGuaranteeReimbursement": "string",
              "shippingFeeSubsidyAmount": "string"
            },
            "tiktokShopShippingIncentiveAmount": "string"
          },
          "skuId": "string",
          "skuName": "Ava Chen",
          "statementId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `feeAndTaxAmount` | string |  |
| `orderCreateTime` | number |  |
| `orderId` | string |  |
| `revenueAmount` | string |  |
| `settlementAmount` | string |  |
| `shippingCostAmount` | string |  |
| `skuTransactions[].feeTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.affiliateAdsCommissionAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.affiliateCommissionAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.affiliateCommissionAmountBeforePit` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.affiliateCommissionDeposit` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.affiliateCommissionRelease` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.affiliatePartnerCommissionAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.autoPostShoppableVideoCommissionFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.bonusCashbackServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.brandAmplificationProgramCommission` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.brandAmplificationProgramFeeTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.brandCampaignFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.brandCampaignFeeTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.buyerFaultReturnShippingFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.campaignPeriodFeeCfpAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.campaignPeriodFeeCfpTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.campaignPeriodFeeSpAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.campaignPeriodFeeSpTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.categoryLedCampaignFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.categoryLedCampaignFeeTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.cofundedCreatorBonusAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.cofundedPromotionServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.cpsShopAdsCommissionTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.creditCardHandlingFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.dtHandlingFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.dynamicCommissionAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.eprPobServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.externalAffiliateMarketingFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.failedDeliveryShippingFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.feePerItemSoldAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.flashSalesServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.gmvMaxAdFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.gmvMaxCouponFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.installationServiceFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.insuranceFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.liveSpecialsFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.mallServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.newCustomerGrowthPackageFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.platformCommissionAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.platformSemiManagedCommissionFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.platformSemiManagedCommissionFeeTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.platformSpecialServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.preOrderServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.referralFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.refundAdministrationFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.sellerGrowthFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.sellerPaylaterHandlingFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.sfpServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.shippingFeeGuaranteeServiceFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.shippingInsuranceFeeTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.smartPromotionFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.storeGmvGrowthPackageFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.tapShopAdsCommission` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.targetProductGmvGrowthPackageFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.transactionFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.tspCommissionAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.vnFixInfrastructureFee` | string |  |
| `skuTransactions[].feeTaxBreakdown.fee.voucherXtraServiceFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.antiDumpingDutyAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.article22IncomeTaxWithheld` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.autoPostShoppableVideoSalesTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.cedularTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.customsClearanceAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.customsDutyAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.gstAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.importVatAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.isrAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.ivaAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.newCustomerGrowthPackageFeeTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.pitAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.salesTaxReferralFeeAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.smartPromotionFeeTaxAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.sstAmount` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.storeGmvGrowthPackageFeeSalesTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.targetProductGmvGrowthPackageTax` | string |  |
| `skuTransactions[].feeTaxBreakdown.tax.vatAmount` | string |  |
| `skuTransactions[].productName` | string |  |
| `skuTransactions[].quantity` | string |  |
| `skuTransactions[].revenueAmount` | string |  |
| `skuTransactions[].revenueBreakdown.codServiceFeeAmount` | string |  |
| `skuTransactions[].revenueBreakdown.distantItemFeeAmount` | string |  |
| `skuTransactions[].revenueBreakdown.refundCodServiceFeeAmount` | string |  |
| `skuTransactions[].revenueBreakdown.refundSubtotalBeforeDiscountAmount` | string |  |
| `skuTransactions[].revenueBreakdown.sellerDiscountAmount` | string |  |
| `skuTransactions[].revenueBreakdown.sellerDiscountRefundAmount` | string |  |
| `skuTransactions[].revenueBreakdown.subtotalBeforeDiscountAmount` | string |  |
| `skuTransactions[].settlementAmount` | string |  |
| `skuTransactions[].shippingCostAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.actualShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.customerPaidShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.distantShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.exchangeShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.failedDeliverySubsidyAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.fbtFreeShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.fbtFulfillmentFeeReimbursementAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.fbtKeyMerchantSubsidy` | string |  |
| `skuTransactions[].shippingCostBreakdown.fbtOverallMerchantSubsidy` | string |  |
| `skuTransactions[].shippingCostBreakdown.freeReturnSubsidyAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.hazmatHandlingFee` | string |  |
| `skuTransactions[].shippingCostBreakdown.hazmatNoncomplianceFee` | string |  |
| `skuTransactions[].shippingCostBreakdown.internationalLegLogisticsAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.logisticsServiceFee` | string |  |
| `skuTransactions[].shippingCostBreakdown.nonStandardDimensionFee` | string |  |
| `skuTransactions[].shippingCostBreakdown.nonStandardWeightFee` | string |  |
| `skuTransactions[].shippingCostBreakdown.replacementShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.returnShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.returnShippingFeePaidBuyerAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.returnShippingLabelFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.sellerSelfShippingServiceFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.shippingAppServiceFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.shippingFeeDiscountAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.shippingInsuranceFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.signatureConfirmationFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.customerShippingFeeOffsetAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.fbmShippingCostAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.fbtFulfillmentFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.fbtShippingCostAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.platformShippingFeeDiscountAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.promoShippingIncentiveAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.refundedCustomerShippingFeeAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.returnRefundSubsidyAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.sellerShippingFeeDiscountAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.shippingFeeGuaranteeReimbursement` | string |  |
| `skuTransactions[].shippingCostBreakdown.supplementaryComponent.shippingFeeSubsidyAmount` | string |  |
| `skuTransactions[].shippingCostBreakdown.tiktokShopShippingIncentiveAmount` | string |  |
| `skuTransactions[].skuId` | string |  |
| `skuTransactions[].skuName` | string |  |
| `skuTransactions[].statementId` | string |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `GET /finance/202501/orders/:order_id/statement_transactions` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions-by-order.md) for the provider-specific parameters and requirements.

