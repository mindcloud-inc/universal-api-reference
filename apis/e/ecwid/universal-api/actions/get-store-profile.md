# Ecwid: Get Store Profile

Retrieves a store profile from Ecwid.

```
GET https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-store-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-store-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-store-profile?${params}`, {
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
      "account": {
        "accountEmail": "ava@example.com",
        "accountName": "Ava Chen",
        "accountNickName": "Ava Chen",
        "availableFeatures": [
          "string"
        ],
        "brandName": "Ava Chen",
        "googlePlaySubscriptionsAvailable": true,
        "itunesSubscriptionsAvailable": true,
        "paid": true,
        "registrationDate": "2026-05-07T12:00:00.000Z",
        "supportEmail": "ava@example.com",
        "suspended": true,
        "trackStorefrontStats": true,
        "whiteLabel": true
      },
      "company": {
        "city": "string",
        "countryCode": "string",
        "email": "ava@example.com",
        "phone": "string",
        "postalCode": "string",
        "stateOrProvinceCode": "string"
      },
      "designSettings": {
        "enableCatalogOnOnePage": true,
        "enableCatalogSeamlessProductListView": true,
        "hideCategoryBlockShowAllEnabledProducts": true,
        "productDetailsAddToCartQuantityCompactView": true,
        "productDetailsDescriptionCompactView": true,
        "productDetailsEstimatedDeliveryTimeCompactView": true,
        "productDetailsExpandedGalleryLayout": "string",
        "productDetailsFavoritesCompactView": true,
        "productDetailsGalleryImagePosition": "string",
        "productDetailsGalleryLayout": "string",
        "productDetailsLayout": "string",
        "productDetailsPositionBreadcrumbs": 1,
        "productDetailsPositionBuyButton": 1,
        "productDetailsPositionProductDescription": 1,
        "productDetailsPositionProductName": 1,
        "productDetailsPositionProductOptions": 1,
        "productDetailsPositionProductPrice": 1,
        "productDetailsPositionProductSku": 1,
        "productDetailsPositionReviewSection": 1,
        "productDetailsPositionSaveForLater": 1,
        "productDetailsPositionShareButtons": 1,
        "productDetailsPositionSizeChart": 1,
        "productDetailsPositionSubtitle": 1,
        "productDetailsPositionWholesalePrices": 1,
        "productDetailsReviewsInSingleViewCompactView": true,
        "productDetailsShareButtonCompactView": true,
        "productDetailsShowAskQuestionSection": true,
        "productDetailsShowAttributes": true,
        "productDetailsShowBreadcrumbs": true,
        "productDetailsShowBreadcrumbsPosition": "string",
        "productDetailsShowDeliveryTime": true,
        "productDetailsShowImageAltTextAsVisibleDescription": true,
        "productDetailsShowInStockLabel": true,
        "productDetailsShowNavigationArrows": true,
        "productDetailsShowNumberOfItemsInStock": true,
        "productDetailsShowPricePerUnit": true,
        "productDetailsShowProductDescription": true,
        "productDetailsShowProductName": true,
        "productDetailsShowProductOptions": true,
        "productDetailsShowProductPhotoZoom": true,
        "productDetailsShowProductPrice": true,
        "productDetailsShowProductSku": true,
        "productDetailsShowQty": true,
        "productDetailsShowRatingSection": true,
        "productDetailsShowReviewsSection": true,
        "productDetailsShowReviewsSectionInOneCardView": true,
        "productDetailsShowSalePrice": true,
        "productDetailsShowSaveForLater": true,
        "productDetailsShowShareButtons": true,
        "productDetailsShowSubtitle": true,
        "productDetailsShowTax": true,
        "productDetailsShowWeight": true,
        "productDetailsShowWholesalePrices": true,
        "productDetailsStockPerOutletCompactView": true,
        "productDetailsTwoColumnsWithLeftSidebarShowProductDescriptionOnSidebar": true,
        "productDetailsTwoColumnsWithRightSidebarShowProductDescriptionOnSidebar": true,
        "productDetailsWholesalePricesCompactView": true,
        "productFiltersOpenedByDefaultOnCatalogPages": true,
        "productFiltersOpenedByDefaultOnCategoryPage": true,
        "productFiltersOrientation": "string",
        "productFiltersPositionCategoryPage": "string",
        "productFiltersPositionOnCatalogPages": "string",
        "productFiltersPositionSearchPage": "string",
        "productFiltersVisibleOnCatalogPages": true,
        "productListBuybuttonBehavior": "string",
        "productListCardSpacingType": "string",
        "productListCategoryTitleBehavior": "string",
        "productListImageAspectRatio": "string",
        "productListImageHasShadow": true,
        "productListImageSize": "string",
        "productListPriceBehavior": "string",
        "productListProductInfoLayout": "string",
        "productListRatingSectionBehavior": "string",
        "productListShowAdditionalImageOnHover": true,
        "productListShowFrame": true,
        "productListShowRatingInOneStar": true,
        "productListShowRatingNumberInFiveStarsView": true,
        "productListShowReviewsCountInFiveStarsView": true,
        "productListShowSortViewasOptions": true,
        "productListSizeProductOptionBehavior": "string",
        "productListSkuBehavior": "string",
        "productListSubtitlesBehavior": "string",
        "productListSwatchesProductOptionBehavior": "string",
        "productListTitleBehavior": "string",
        "shoppingCartProductsCollapsedOnDesktop": true,
        "shoppingCartProductsCollapsedOnMobile": true,
        "showBreadcrumbs": true,
        "showFooterMenu": true,
        "showSigninLink": true,
        "showSigninLinkWithUnifiedAccountPage": true,
        "swatchesProductOptionShape": "string",
        "swatchesProductOptionSize": "string"
      },
      "featureToggles": [
        {
          "enabled": true,
          "name": "Ava Chen",
          "visible": true
        }
      ],
      "formatsAndUnits": {
        "addressFormat": {
          "multiline": "string",
          "plain": "string"
        },
        "currency": "string",
        "currencyDecimalSeparator": "string",
        "currencyGroupSeparator": "string",
        "currencyPrecision": 1,
        "currencyPrefix": "string",
        "currencyRate": 1,
        "currencySuffix": "string",
        "currencyTruncateZeroFractional": true,
        "dateFormat": "string",
        "dimensionsUnit": "string",
        "orderNumberPrefix": "string",
        "orderNumberSuffix": "string",
        "timeFormat": "string",
        "timezone": "string",
        "volumeUnit": "string",
        "weightDecimalSeparator": "string",
        "weightGroupSeparator": "string",
        "weightTruncateZeroFractional": true,
        "weightUnit": "string"
      },
      "generalInfo": {
        "instantSiteV2Enabled": true,
        "profileId": "string",
        "starterSite": {
          "ecwidSubdomain": "string",
          "ecwidSubdomainSuffix": "string",
          "generatedUrl": "https://example.com",
          "slugsWithoutIdsEnabled": true
        },
        "storefrontUrlFormat": "https://example.com",
        "storefrontUrlSlugFormat": "https://example.com",
        "storeId": 1,
        "storeUrl": "https://example.com",
        "websitePlatform": "string"
      },
      "languages": {
        "defaultLanguage": "string",
        "enabledLanguages": [
          "string"
        ],
        "facebookPreferredLocale": "string"
      },
      "legalPagesSettings": {
        "legalPages": [
          {
            "display": "string",
            "displayTranslated": {
              "es": "string"
            },
            "enabled": true,
            "externalUrl": "https://example.com",
            "externalUrlTranslated": {
              "es": "https://example.com"
            },
            "text": "string",
            "textTranslated": {
              "es": "string"
            },
            "title": "string",
            "titleTranslated": {
              "es": "string"
            },
            "type": "string"
          }
        ],
        "requireTermsAgreementAtCheckout": true
      },
      "mailNotifications": {
        "adminMessages": {
          "lowStockNotification": {
            "enabled": true
          },
          "newOrderPlaced": {
            "enabled": true
          },
          "weeklyStatsReport": {
            "enabled": true
          }
        },
        "adminNotificationEmails": [
          "ava@example.com"
        ],
        "customerMarketingMessages": {
          "abandonedCartRecovery": {
            "enabled": true,
            "marketingBlockEnabled": true
          },
          "customerLoyaltyAppreciation": {
            "enabled": true
          },
          "favoriteProductsReminder": {
            "enabled": true
          },
          "feedbackRequest": {
            "enabled": true
          },
          "inactiveCustomerReminder": {
            "enabled": true
          },
          "purchaseAnniversary": {
            "enabled": true
          }
        },
        "customerNotificationFromEmail": "ava@example.com",
        "customerOrderMessages": {
          "downloadEgoods": {
            "enabled": true
          },
          "orderConfirmation": {
            "enabled": true,
            "marketingBlockEnabled": true
          },
          "orderDelivered": {
            "enabled": true
          },
          "orderIsReadyForPickup": {
            "enabled": true
          },
          "orderShipped": {
            "enabled": true
          },
          "orderStatusChanged": {
            "enabled": true
          }
        }
      },
      "payment": {
        "applePay": {
          "available": true,
          "enabled": true
        },
        "countryCode": "string",
        "paymentOptions": [
          {
            "appClientId": "string",
            "appNamespace": "Ava Chen",
            "checkoutDescription": "string",
            "checkoutTitle": "string",
            "checkoutTitleTranslated": {
              "es": "string"
            },
            "configured": true,
            "enabled": true,
            "id": "string",
            "instructionsForCustomer": {
              "instructions": "string",
              "instructionsTitle": "string",
              "instructionsTranslated": {
                "es": "string"
              }
            },
            "orderBy": 1,
            "paymentProcessorId": "string",
            "paymentProcessorTitle": "string"
          }
        ]
      },
      "productFiltersSettings": {
        "enabledInStorefront": true
      },
      "registrationAnswers": {
        "alreadySelling": "string",
        "ecom": "string",
        "forSomeone": "string",
        "goods": "string",
        "platform": "string",
        "pos": "string",
        "website": "string"
      },
      "settings": {
        "abandonedSales": {
          "autoAbandonedSalesRecovery": true
        },
        "acceptMarketingCheckboxCustomText": "string",
        "acceptMarketingCheckboxCustomTextTranslated": {
          "es": "string"
        },
        "acceptMarketingCheckboxDefaultValue": true,
        "askCompanyName": true,
        "askConsentToTrackInStorefront": true,
        "askTaxId": true,
        "askZipCode": true,
        "closed": true,
        "defaultAllProductsViewSortOrder": "string",
        "defaultProductSortOrder": "string",
        "favoritesEnabled": true,
        "googleRemarketingEnabled": true,
        "hideOutOfStockProductsInStorefront": true,
        "highlightCompositeProductsOnStorefront": "string",
        "linkUpEnabled": true,
        "openBagOnAddition": true,
        "orderCommentsCaption": "string",
        "orderCommentsCaptionTranslated": {
          "es": "string"
        },
        "orderCommentsEnabled": true,
        "orderCommentsRequired": true,
        "productCondition": "string",
        "productReviewsFeatureEnabled": true,
        "productSortOrderInCart": "string",
        "recurringSubscriptionsSettings": {
          "showRecurringSubscriptionsInControlPanel": true,
          "supportedPaymentMethodsStatuses": {
            "supportedPaymentMethodsAreAvailable": true,
            "supportedPaymentMethodsAreConnected": true
          }
        },
        "requirePhoneOnCheckout": true,
        "rootCategorySeoDescription": "string",
        "rootCategorySeoDescriptionTranslated": {
          "es": "string"
        },
        "rootCategorySeoTitleTranslated": {
          "es": "string"
        },
        "salePrice": {
          "displayDiscount": "string",
          "displayLowestPrice": true,
          "displayOnProductList": true,
          "oldPriceLabelTranslated": {
            "es": "string"
          }
        },
        "showAcceptMarketingCheckbox": true,
        "showPricePerUnit": true,
        "showRepeatOrderButton": true,
        "storeDescriptionTranslated": {
          "es": "string"
        },
        "storeName": "Ava Chen",
        "wixExternalTrackingEnabled": true
      },
      "shipping": {
        "handlingFee": {
          "value": 1
        },
        "shippingOrigin": {
          "city": "string",
          "countryCode": "string",
          "countryName": "Ava Chen",
          "phone": "string",
          "postalCode": "string",
          "stateOrProvinceCode": "string"
        }
      },
      "taxInvoiceSettings": {
        "attachTaxInvoiceToOrderEmailNotifications": "ava@example.com",
        "enableTaxInvoices": true,
        "generateInvoicesAutomatically": "string"
      },
      "taxSettings": {
        "automaticTaxEnabled": true,
        "b2bB2c": "string",
        "electronicInvoiceFieldsAtCheckoutEnabled": true,
        "euIossEnabled": true,
        "pricesIncludeTax": true,
        "taxExemptBusiness": true,
        "taxOnShippingCalculationScheme": "string",
        "ukVatRegistered": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountEmail` | string |  |
| `account.accountName` | string |  |
| `account.accountNickName` | string |  |
| `account.availableFeatures[]` | string |  |
| `account.brandName` | string |  |
| `account.googlePlaySubscriptionsAvailable` | boolean |  |
| `account.itunesSubscriptionsAvailable` | boolean |  |
| `account.paid` | boolean |  |
| `account.registrationDate` | date |  |
| `account.supportEmail` | string |  |
| `account.suspended` | boolean |  |
| `account.trackStorefrontStats` | boolean |  |
| `account.whiteLabel` | boolean |  |
| `company.city` | string |  |
| `company.countryCode` | string |  |
| `company.email` | string |  |
| `company.phone` | string |  |
| `company.postalCode` | string |  |
| `company.stateOrProvinceCode` | string |  |
| `designSettings.enableCatalogOnOnePage` | boolean |  |
| `designSettings.enableCatalogSeamlessProductListView` | boolean |  |
| `designSettings.hideCategoryBlockShowAllEnabledProducts` | boolean |  |
| `designSettings.productDetailsAddToCartQuantityCompactView` | boolean |  |
| `designSettings.productDetailsDescriptionCompactView` | boolean |  |
| `designSettings.productDetailsEstimatedDeliveryTimeCompactView` | boolean |  |
| `designSettings.productDetailsExpandedGalleryLayout` | string |  |
| `designSettings.productDetailsFavoritesCompactView` | boolean |  |
| `designSettings.productDetailsGalleryImagePosition` | string |  |
| `designSettings.productDetailsGalleryLayout` | string |  |
| `designSettings.productDetailsLayout` | string |  |
| `designSettings.productDetailsPositionBreadcrumbs` | number |  |
| `designSettings.productDetailsPositionBuyButton` | number |  |
| `designSettings.productDetailsPositionProductDescription` | number |  |
| `designSettings.productDetailsPositionProductName` | number |  |
| `designSettings.productDetailsPositionProductOptions` | number |  |
| `designSettings.productDetailsPositionProductPrice` | number |  |
| `designSettings.productDetailsPositionProductSku` | number |  |
| `designSettings.productDetailsPositionReviewSection` | number |  |
| `designSettings.productDetailsPositionSaveForLater` | number |  |
| `designSettings.productDetailsPositionShareButtons` | number |  |
| `designSettings.productDetailsPositionSizeChart` | number |  |
| `designSettings.productDetailsPositionSubtitle` | number |  |
| `designSettings.productDetailsPositionWholesalePrices` | number |  |
| `designSettings.productDetailsReviewsInSingleViewCompactView` | boolean |  |
| `designSettings.productDetailsShareButtonCompactView` | boolean |  |
| `designSettings.productDetailsShowAskQuestionSection` | boolean |  |
| `designSettings.productDetailsShowAttributes` | boolean |  |
| `designSettings.productDetailsShowBreadcrumbs` | boolean |  |
| `designSettings.productDetailsShowBreadcrumbsPosition` | string |  |
| `designSettings.productDetailsShowDeliveryTime` | boolean |  |
| `designSettings.productDetailsShowImageAltTextAsVisibleDescription` | boolean |  |
| `designSettings.productDetailsShowInStockLabel` | boolean |  |
| `designSettings.productDetailsShowNavigationArrows` | boolean |  |
| `designSettings.productDetailsShowNumberOfItemsInStock` | boolean |  |
| `designSettings.productDetailsShowPricePerUnit` | boolean |  |
| `designSettings.productDetailsShowProductDescription` | boolean |  |
| `designSettings.productDetailsShowProductName` | boolean |  |
| `designSettings.productDetailsShowProductOptions` | boolean |  |
| `designSettings.productDetailsShowProductPhotoZoom` | boolean |  |
| `designSettings.productDetailsShowProductPrice` | boolean |  |
| `designSettings.productDetailsShowProductSku` | boolean |  |
| `designSettings.productDetailsShowQty` | boolean |  |
| `designSettings.productDetailsShowRatingSection` | boolean |  |
| `designSettings.productDetailsShowReviewsSection` | boolean |  |
| `designSettings.productDetailsShowReviewsSectionInOneCardView` | boolean |  |
| `designSettings.productDetailsShowSalePrice` | boolean |  |
| `designSettings.productDetailsShowSaveForLater` | boolean |  |
| `designSettings.productDetailsShowShareButtons` | boolean |  |
| `designSettings.productDetailsShowSubtitle` | boolean |  |
| `designSettings.productDetailsShowTax` | boolean |  |
| `designSettings.productDetailsShowWeight` | boolean |  |
| `designSettings.productDetailsShowWholesalePrices` | boolean |  |
| `designSettings.productDetailsStockPerOutletCompactView` | boolean |  |
| `designSettings.productDetailsTwoColumnsWithLeftSidebarShowProductDescriptionOnSidebar` | boolean |  |
| `designSettings.productDetailsTwoColumnsWithRightSidebarShowProductDescriptionOnSidebar` | boolean |  |
| `designSettings.productDetailsWholesalePricesCompactView` | boolean |  |
| `designSettings.productFiltersOpenedByDefaultOnCatalogPages` | boolean |  |
| `designSettings.productFiltersOpenedByDefaultOnCategoryPage` | boolean |  |
| `designSettings.productFiltersOrientation` | string |  |
| `designSettings.productFiltersPositionCategoryPage` | string |  |
| `designSettings.productFiltersPositionOnCatalogPages` | string |  |
| `designSettings.productFiltersPositionSearchPage` | string |  |
| `designSettings.productFiltersVisibleOnCatalogPages` | boolean |  |
| `designSettings.productListBuybuttonBehavior` | string |  |
| `designSettings.productListCardSpacingType` | string |  |
| `designSettings.productListCategoryTitleBehavior` | string |  |
| `designSettings.productListImageAspectRatio` | string |  |
| `designSettings.productListImageHasShadow` | boolean |  |
| `designSettings.productListImageSize` | string |  |
| `designSettings.productListPriceBehavior` | string |  |
| `designSettings.productListProductInfoLayout` | string |  |
| `designSettings.productListRatingSectionBehavior` | string |  |
| `designSettings.productListShowAdditionalImageOnHover` | boolean |  |
| `designSettings.productListShowFrame` | boolean |  |
| `designSettings.productListShowRatingInOneStar` | boolean |  |
| `designSettings.productListShowRatingNumberInFiveStarsView` | boolean |  |
| `designSettings.productListShowReviewsCountInFiveStarsView` | boolean |  |
| `designSettings.productListShowSortViewasOptions` | boolean |  |
| `designSettings.productListSizeProductOptionBehavior` | string |  |
| `designSettings.productListSkuBehavior` | string |  |
| `designSettings.productListSubtitlesBehavior` | string |  |
| `designSettings.productListSwatchesProductOptionBehavior` | string |  |
| `designSettings.productListTitleBehavior` | string |  |
| `designSettings.shoppingCartProductsCollapsedOnDesktop` | boolean |  |
| `designSettings.shoppingCartProductsCollapsedOnMobile` | boolean |  |
| `designSettings.showBreadcrumbs` | boolean |  |
| `designSettings.showFooterMenu` | boolean |  |
| `designSettings.showSigninLink` | boolean |  |
| `designSettings.showSigninLinkWithUnifiedAccountPage` | boolean |  |
| `designSettings.swatchesProductOptionShape` | string |  |
| `designSettings.swatchesProductOptionSize` | string |  |
| `featureToggles[].enabled` | boolean |  |
| `featureToggles[].name` | string |  |
| `featureToggles[].visible` | boolean |  |
| `formatsAndUnits.addressFormat.multiline` | string |  |
| `formatsAndUnits.addressFormat.plain` | string |  |
| `formatsAndUnits.currency` | string |  |
| `formatsAndUnits.currencyDecimalSeparator` | string |  |
| `formatsAndUnits.currencyGroupSeparator` | string |  |
| `formatsAndUnits.currencyPrecision` | number |  |
| `formatsAndUnits.currencyPrefix` | string |  |
| `formatsAndUnits.currencyRate` | number |  |
| `formatsAndUnits.currencySuffix` | string |  |
| `formatsAndUnits.currencyTruncateZeroFractional` | boolean |  |
| `formatsAndUnits.dateFormat` | string |  |
| `formatsAndUnits.dimensionsUnit` | string |  |
| `formatsAndUnits.orderNumberPrefix` | string |  |
| `formatsAndUnits.orderNumberSuffix` | string |  |
| `formatsAndUnits.timeFormat` | string |  |
| `formatsAndUnits.timezone` | string |  |
| `formatsAndUnits.volumeUnit` | string |  |
| `formatsAndUnits.weightDecimalSeparator` | string |  |
| `formatsAndUnits.weightGroupSeparator` | string |  |
| `formatsAndUnits.weightTruncateZeroFractional` | boolean |  |
| `formatsAndUnits.weightUnit` | string |  |
| `generalInfo.instantSiteV2Enabled` | boolean |  |
| `generalInfo.profileId` | string |  |
| `generalInfo.starterSite.ecwidSubdomain` | string |  |
| `generalInfo.starterSite.ecwidSubdomainSuffix` | string |  |
| `generalInfo.starterSite.generatedUrl` | string |  |
| `generalInfo.starterSite.slugsWithoutIdsEnabled` | boolean |  |
| `generalInfo.storefrontUrlFormat` | string |  |
| `generalInfo.storefrontUrlSlugFormat` | string |  |
| `generalInfo.storeId` | number |  |
| `generalInfo.storeUrl` | string |  |
| `generalInfo.websitePlatform` | string |  |
| `languages.defaultLanguage` | string |  |
| `languages.enabledLanguages[]` | string |  |
| `languages.facebookPreferredLocale` | string |  |
| `legalPagesSettings.legalPages[].display` | string |  |
| `legalPagesSettings.legalPages[].displayTranslated.es` | string |  |
| `legalPagesSettings.legalPages[].enabled` | boolean |  |
| `legalPagesSettings.legalPages[].externalUrl` | string |  |
| `legalPagesSettings.legalPages[].externalUrlTranslated.es` | string |  |
| `legalPagesSettings.legalPages[].text` | string |  |
| `legalPagesSettings.legalPages[].textTranslated.es` | string |  |
| `legalPagesSettings.legalPages[].title` | string |  |
| `legalPagesSettings.legalPages[].titleTranslated.es` | string |  |
| `legalPagesSettings.legalPages[].type` | string |  |
| `legalPagesSettings.requireTermsAgreementAtCheckout` | boolean |  |
| `mailNotifications.adminMessages.lowStockNotification.enabled` | boolean |  |
| `mailNotifications.adminMessages.newOrderPlaced.enabled` | boolean |  |
| `mailNotifications.adminMessages.weeklyStatsReport.enabled` | boolean |  |
| `mailNotifications.adminNotificationEmails[]` | string |  |
| `mailNotifications.customerMarketingMessages.abandonedCartRecovery.enabled` | boolean |  |
| `mailNotifications.customerMarketingMessages.abandonedCartRecovery.marketingBlockEnabled` | boolean |  |
| `mailNotifications.customerMarketingMessages.customerLoyaltyAppreciation.enabled` | boolean |  |
| `mailNotifications.customerMarketingMessages.favoriteProductsReminder.enabled` | boolean |  |
| `mailNotifications.customerMarketingMessages.feedbackRequest.enabled` | boolean |  |
| `mailNotifications.customerMarketingMessages.inactiveCustomerReminder.enabled` | boolean |  |
| `mailNotifications.customerMarketingMessages.purchaseAnniversary.enabled` | boolean |  |
| `mailNotifications.customerNotificationFromEmail` | string |  |
| `mailNotifications.customerOrderMessages.downloadEgoods.enabled` | boolean |  |
| `mailNotifications.customerOrderMessages.orderConfirmation.enabled` | boolean |  |
| `mailNotifications.customerOrderMessages.orderConfirmation.marketingBlockEnabled` | boolean |  |
| `mailNotifications.customerOrderMessages.orderDelivered.enabled` | boolean |  |
| `mailNotifications.customerOrderMessages.orderIsReadyForPickup.enabled` | boolean |  |
| `mailNotifications.customerOrderMessages.orderShipped.enabled` | boolean |  |
| `mailNotifications.customerOrderMessages.orderStatusChanged.enabled` | boolean |  |
| `payment.applePay.available` | boolean |  |
| `payment.applePay.enabled` | boolean |  |
| `payment.countryCode` | string |  |
| `payment.paymentOptions[].appClientId` | string |  |
| `payment.paymentOptions[].appNamespace` | string |  |
| `payment.paymentOptions[].checkoutDescription` | string |  |
| `payment.paymentOptions[].checkoutTitle` | string |  |
| `payment.paymentOptions[].checkoutTitleTranslated.es` | string |  |
| `payment.paymentOptions[].configured` | boolean |  |
| `payment.paymentOptions[].enabled` | boolean |  |
| `payment.paymentOptions[].id` | string |  |
| `payment.paymentOptions[].instructionsForCustomer.instructions` | string |  |
| `payment.paymentOptions[].instructionsForCustomer.instructionsTitle` | string |  |
| `payment.paymentOptions[].instructionsForCustomer.instructionsTranslated.es` | string |  |
| `payment.paymentOptions[].orderBy` | number |  |
| `payment.paymentOptions[].paymentProcessorId` | string |  |
| `payment.paymentOptions[].paymentProcessorTitle` | string |  |
| `productFiltersSettings.enabledInStorefront` | boolean |  |
| `registrationAnswers.alreadySelling` | string |  |
| `registrationAnswers.ecom` | string |  |
| `registrationAnswers.forSomeone` | string |  |
| `registrationAnswers.goods` | string |  |
| `registrationAnswers.platform` | string |  |
| `registrationAnswers.pos` | string |  |
| `registrationAnswers.website` | string |  |
| `settings.abandonedSales.autoAbandonedSalesRecovery` | boolean |  |
| `settings.acceptMarketingCheckboxCustomText` | string |  |
| `settings.acceptMarketingCheckboxCustomTextTranslated.es` | string |  |
| `settings.acceptMarketingCheckboxDefaultValue` | boolean |  |
| `settings.askCompanyName` | boolean |  |
| `settings.askConsentToTrackInStorefront` | boolean |  |
| `settings.askTaxId` | boolean |  |
| `settings.askZipCode` | boolean |  |
| `settings.closed` | boolean |  |
| `settings.defaultAllProductsViewSortOrder` | string |  |
| `settings.defaultProductSortOrder` | string |  |
| `settings.favoritesEnabled` | boolean |  |
| `settings.googleRemarketingEnabled` | boolean |  |
| `settings.hideOutOfStockProductsInStorefront` | boolean |  |
| `settings.highlightCompositeProductsOnStorefront` | string |  |
| `settings.linkUpEnabled` | boolean |  |
| `settings.openBagOnAddition` | boolean |  |
| `settings.orderCommentsCaption` | string |  |
| `settings.orderCommentsCaptionTranslated.es` | string |  |
| `settings.orderCommentsEnabled` | boolean |  |
| `settings.orderCommentsRequired` | boolean |  |
| `settings.productCondition` | string |  |
| `settings.productReviewsFeatureEnabled` | boolean |  |
| `settings.productSortOrderInCart` | string |  |
| `settings.recurringSubscriptionsSettings.showRecurringSubscriptionsInControlPanel` | boolean |  |
| `settings.recurringSubscriptionsSettings.supportedPaymentMethodsStatuses.supportedPaymentMethodsAreAvailable` | boolean |  |
| `settings.recurringSubscriptionsSettings.supportedPaymentMethodsStatuses.supportedPaymentMethodsAreConnected` | boolean |  |
| `settings.requirePhoneOnCheckout` | boolean |  |
| `settings.rootCategorySeoDescription` | string |  |
| `settings.rootCategorySeoDescriptionTranslated.es` | string |  |
| `settings.rootCategorySeoTitleTranslated.es` | string |  |
| `settings.salePrice.displayDiscount` | string |  |
| `settings.salePrice.displayLowestPrice` | boolean |  |
| `settings.salePrice.displayOnProductList` | boolean |  |
| `settings.salePrice.oldPriceLabelTranslated.es` | string |  |
| `settings.showAcceptMarketingCheckbox` | boolean |  |
| `settings.showPricePerUnit` | boolean |  |
| `settings.showRepeatOrderButton` | boolean |  |
| `settings.storeDescriptionTranslated.es` | string |  |
| `settings.storeName` | string |  |
| `settings.wixExternalTrackingEnabled` | boolean |  |
| `shipping.handlingFee.value` | number |  |
| `shipping.shippingOrigin.city` | string |  |
| `shipping.shippingOrigin.countryCode` | string |  |
| `shipping.shippingOrigin.countryName` | string |  |
| `shipping.shippingOrigin.phone` | string |  |
| `shipping.shippingOrigin.postalCode` | string |  |
| `shipping.shippingOrigin.stateOrProvinceCode` | string |  |
| `taxInvoiceSettings.attachTaxInvoiceToOrderEmailNotifications` | string |  |
| `taxInvoiceSettings.enableTaxInvoices` | boolean |  |
| `taxInvoiceSettings.generateInvoicesAutomatically` | string |  |
| `taxSettings.automaticTaxEnabled` | boolean |  |
| `taxSettings.b2bB2c` | string |  |
| `taxSettings.electronicInvoiceFieldsAtCheckoutEnabled` | boolean |  |
| `taxSettings.euIossEnabled` | boolean |  |
| `taxSettings.pricesIncludeTax` | boolean |  |
| `taxSettings.taxExemptBusiness` | boolean |  |
| `taxSettings.taxOnShippingCalculationScheme` | string |  |
| `taxSettings.ukVatRegistered` | boolean |  |

## Native endpoint

Through the native Ecwid API, this operation is `GET /:storeId/profile` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store-profile.md) for the provider-specific parameters and requirements.

