# Changelog

Field changes in each published JSON-LD context, compared with the previous release:

## [v1rc5](https://w3id.org/vvc/v1rc5) - Unreleased

### Added
- `VehicleTitle`, `VehicleRegistration`, and `VehicleInsuranceInformation`:
  - `make`
  - `makeCode`
- `VehicleTitle`:
  - `jurisdiction`
  - `titleNumber`

### Changed
- Renamed `designations` to `branding` in `VehicleTitle` and clarified the title brand description.

## [v1rc4](https://w3id.org/vvc/v1rc4) - 2026-09-15

### Added
- `CoverageLimit`:
  - `coverageType`
  - `coverageLimitPerAccident`
  - `coverageLimitPerPerson`
- `ProofOfInsuranceCredential` (also in `VehicleInsuranceInformation`, except `issuingBureau`):
  - `coverageLimit`
  - `insuredAddress`
  - `insurerCode`
  - `issuingBureau`
  - `jurisdictionValidity`
  - `minimumLegalCoverageConfirmed`
  - `naicNumber`
  - `namedInsured`
- `VehicleRegistration`:
  - `feeBasisYear`
  - `licenseTypeCode`
  - `registrationIssueDate`
  - `vlfClass`
- `VehicleTitle`:
  - `firstSold`

### Changed
- Renamed `vehicleType` to `vehicleTypeCode`.
- `purchaseDate` and `vehicleModelDate` use `xsd:date`; `numberOfAxles` uses
  `xsd:integer`.
- `bodyType`, `brand`, `fuelType`, `manufacturer`, `numberOfAxles`,
  `vehicleIdentificationNumber`, `vehicleModelDate`, and `weight` use VVC mappings.
  Remaining schema.org mappings use HTTPS.
- `brand`, `coverageAmount`, `insuranceProvider`, `manufacturer`,
  `registeringOrganization`, and `weight` use `@id` values.

### Removed
- `registrationExpirationDate` from `VehicleTitle` and `class` from
  `VehicleRegistration`.
- Scoped `class`, `month`, and `year` fields from `FirstSaleInformation`.

## [v1rc3](https://w3id.org/vvc/v1rc3) - 2026-01-12

### Added
- `VehicleTitle`, `VehicleRegistration`, and `VehicleInsuranceInformation`:
  - `model`
  - `numberOfCylinders`
  - `vehicleType`
  - `vesselType`
  - `weightClass`
- `VehicleTitle` and `VehicleRegistration`:
  - `feesPaid`
  - `isInsured`
  - `motivePower`
- `VehicleRegistration`:
  - `class`
- `VehicleInsuranceInformation`:
  - `brand`
  - `numberOfAxles`

### Changed
- `lienholder` uses `@id` values; `vehicleModelDate` uses `xsd:dateTime`.
- Removed explicit `xsd:unsignedInt` types from `numberOfAxles` and `Observation.value`.
- Schema.org mappings use HTTP. Nested contexts are protected and define local `id` and
  `type` aliases.

## [v1rc2](https://w3id.org/vvc/v1rc2) - 2026-01-12

### Added
- `VehicleInsuranceCredential` and `VehicleInsuranceInformation` with shared vehicle
  fields and:
  - `coverageAmount`
  - `insuranceProvider`
  - `policyEndDate`
  - `policyHolder`
  - `policyNumber`
  - `policyStartDate`
- `VehicleRegistrationCredential` and `VehicleRegistration` with shared vehicle fields
  and:
  - `registeringOrganization`
  - `registrationStartDate`

### Changed
- Replaced `VehicleCredential` and `Vehicle` with `VehicleTitleCredential` and
  `VehicleTitle`, retaining the vehicle fields.

## [v1rc1](https://w3id.org/vvc/v1rc1) - 2026-01-12

### Added
- Initial `VehicleCredential` and `Vehicle` terms.
- Vehicle fields:
  - `bodyType`
  - `brand`
  - `controlNumber`
  - `designations`
  - `equipmentTrustNumber`
  - `fuelType`
  - `licensePlateIdentifier`
  - `lienholder`
  - `lienholderReleaseDate`
  - `manufacturer`
  - `motorcycleEngineNumber`
  - `numberOfAxles`
  - `odometerReading`
  - `owner`
  - `ownerSaleRequirements`
  - `provenanceResource`
  - `purchaseDate`
  - `registrationExpirationDate`
  - `titleIssueDate`
  - `vehicleIdentificationNumber`
  - `vehicleModelDate`
  - `weight`
- `Person` and `Organization`:
  - `address`
  - `description`
  - `hasCertification`
  - `name`
- `PostalAddress`:
  - `addressLocality`
  - `addressRegion`
  - `postalCode`
  - `streetAddress`
- `Observation`:
  - `description`
  - `observationDate`
  - `unitCode`
  - `value`
  - `variableMeasured`
- `Certification`:
  - `about`
  - `certificationIdentification`
- `MonetaryAmount`:
  - `currency`
  - `value`
- `QuantitativeValue`:
  - `unitCode`
  - `value`
- `FirstSaleInformation`:
  - `class`
  - `month`
  - `year`
