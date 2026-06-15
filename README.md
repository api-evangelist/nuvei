# Nuvei (nuvei)

Nuvei is a global payment technology company headquartered in Montreal, Canada, providing a single platform for online card acquiring, alternative payment methods (700+ APMs), payouts, currency management across 150+ currencies, risk and fraud, and payment orchestration. Nuvei serves merchants in 200+ markets with local acquiring in 52 markets across eCommerce, iGaming, sports betting, travel, retail, B2B, and financial services. Originally listed on Nasdaq and TSX as NVEI, Nuvei was taken private by Advent International in 2024.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/nuvei/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/nuvei/refs/heads/main/apis.yml)

## Tags

- Payments
- Payment Processing
- Payment Gateway
- Acquiring
- Payouts
- Alternative Payment Methods
- Fraud
- Risk
- Currency Conversion
- iGaming
- eCommerce
- FinTech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Nuvei Payments API

Server-to-server REST API for processing card and APM transactions through Nuvei. Includes openOrder for session setup, payment for end-to-end transactions, settleTransaction for capturing pre-authorized amounts, refundTransaction for refunds, voidTransaction for cancellations, and getPaymentStatus for transaction state. Auth uses SHA-256 checksum over merchantId, merchantSiteId, clientRequestId, amount, currency, timeStamp, and merchantSecretKey.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Payments
- Authorization
- Settlement
- Refund
- Void

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-payments-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-payments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/nuvei-payment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/nuvei-transaction-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Nuvei Session API

Generates and manages session tokens (getSessionToken) used to authenticate subsequent REST calls and Web SDK operations. Session tokens are scoped to a merchant and order and have a short lifetime.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Sessions
- Tokens
- Authentication

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-session-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-session-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-session-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Order API

Creates and updates orders prior to payment via openOrder and updateOrder. Supports line items, billing/shipping addresses, currency, device details, and dynamic descriptors. Used as the first step for Web SDK, Simply Connect, and Payment Page integrations.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Orders
- Cart
- Checkout

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-order-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-order-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-order-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Payouts API

Pushes funds out to consumers and counterparties via card, bank account, and a wide set of local APMs. The payout endpoint supports referenced (relatedTransactionId) and unreferenced (account number / IBAN) payouts and integrates with accountCapture to collect destination details safely.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Payouts
- Withdrawals
- Disbursement

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-payouts-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-payouts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payouts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei User Payment Options API

Manages stored payment instruments (User Payment Options / UPOs) including card and APM tokenization. Supports addUPOCreditCard, addUPOAPM, editUPOCreditCard, editUPOAPM, deleteUPO, getUserUPOs, and enableUPO/disableUPO.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Tokens
- Vault
- User Payment Options
- Cards

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-user-payment-options-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-user-payment-options-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-user-payment-options-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Merchant Configuration API

Returns configuration data for a merchant including supported countries (getMerchantCountries) and the active set of payment methods per country (getMerchantPaymentMethods). Used by client checkouts to render dynamic payment selection.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- Merchant
- Configuration
- Payment Methods
- Countries

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-merchant-config-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-merchant-config-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-merchant-config-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei 3DS API

3D Secure 2 authentication endpoints. getCard3DDetails returns DS information and challenge requirements for a card; authenticate3d completes the authentication flow returning CAVV and ECI. Designed to satisfy PSD2 SCA requirements for EEA acquiring.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- 3DS
- SCA
- Authentication
- Cards

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-3ds-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-3ds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-3ds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei DCC API

Dynamic Currency Conversion. getDccDetails computes the converted amount and markup rate for a card BIN and currency pair so merchants can present a localized currency offer at checkout.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- **Base URL:** `https://secure.safecharge.com/ppp/api/v1/`

#### Tags

- DCC
- Currency Conversion
- FX

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-dcc-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/nuvei-dcc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-dcc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Nuvei Direct Merchant Notifications (DMN)

Asynchronous webhook notifications sent from Nuvei to a merchant endpoint to communicate the final status of payments, payouts, refunds, voids, settles, and Control Panel events. Payment DMNs include an advanceResponseChecksum signed with the merchantSecretKey using SHA-256 over the ordered parameter values; withdrawal DMNs concatenate name=value pairs with the secret appended.

- **Human URL:** [https://docs.nuvei.com/documentation/integration/webhooks/](https://docs.nuvei.com/documentation/integration/webhooks/)

#### Tags

- Webhooks
- Events
- Notifications
- DMN

#### Properties

- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/)
- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/payment-dmns/)
- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/withdrawal-dmns/)
- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/control-panel/)
- [AsyncAPI](asyncapi/nuvei-dmn-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/nuvei-3ds-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-3ds-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-dcc-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-dcc-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-merchant-config-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-merchant-config-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-order-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-order-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-payments-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payments-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-payouts-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-payouts-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-session-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-session-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/nuvei-user-payment-options-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/nuvei-user-payment-options-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [SDK](https://github.com/Nuvei/nuvei-server-php)
- [SDK](https://github.com/Nuvei/nuvei-server-java)
- [SDK](https://github.com/Nuvei/nuvei-server-java-2.0)
- [SDK](https://github.com/Nuvei/nuvei-server-nodejs)
- [SDK](https://github.com/Nuvei/nuvei-mobile-sdk-android)
- [SDK](https://github.com/Nuvei/nuvei-mobile-sdk-ios)
- [SDK](https://github.com/Nuvei/nuvei-react-native-mobile-sdk)
- [SDK](https://github.com/Nuvei/nuvei-mobile-cashier-helper-android)
- [SDK](https://github.com/Nuvei/nuvei-mobile-cashier-helper-ios)
- [SDK](https://github.com/Nuvei/nuvei-cashier-helper-react-for-android)
- [SDK](https://github.com/Nuvei/nuvei-mobile-pods)
- [SDK](https://github.com/Nuvei/nuvei-maven-android)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-magento-2)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-woocommerce)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-prestashop)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-opencart-3)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-opencart-4)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-shopware-5)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-shopware-6)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-salesforce-commerce-cloud)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-sap-commerce)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-commerce-tools-backend)
- [Plugin](https://github.com/Nuvei/nuvei-plugin-commerce-tools-frontend)

## Maintainers

**FN:** Kin Lane
**URL:** https://kinlane.com
