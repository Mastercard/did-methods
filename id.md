# Introduction

The Mastercard ID platform aims to provide online identity verification for consumers.  As part of this program, we wish to operate the `id` method for representing a user.

# Scheme

The following scheme is proposed:

`did:id:identifier:environment`

In this example, `identifier` is a a UUIDv4, and `environment` is *optional*, and used to further scope requests to different operating environments as necessary.

# CRUD Operations

The following operations are supported:

## Create

TBD

## Retrieve

TBD

## Update

TBD

## Delete

TBD

# Security Considerations

This section provides the security consideration for the DID method implementation.
 - In case of a key compromise, the participant MUST notify governance body and deactivate existing DID immediately.
 - All communication MUST be encrypted using TLS 1.2 and above with 2048-bit key length supporting only secure cryptographic algorithms.
 - The participant server SHOULD be configured to only support strong cipher suites.
 - Any sensitive information SHOULD be shared through TLS and JWE encryption / message level encryption.
 - In case of any security incident, the participant MUST inform governance body.
 - The participant MUST store the private key securely.
 - Participant developers SHOULD NOT write client applications that collect authentication information directly from users and should instead delegate this task to a trusted system component (for example, the system browser).
 - The participant MUST ensure that the application architecture is secure. The participant SHOULD implement necessary security controls to the application and implement an anti-fraud functionality.
 - When the participant invokes DID method from a mobile application, the participant MUST ensure that the mobile application is obfuscated and signed using a trust certificate when available for public distribution.
 - All communication from the participant MUST use OAUTH2 for API authentication with Mastercard ID Service platform. The participant is responsible for generating and storing keys securely on cryptographic storage such as Hardware Security Module (HSM) in their infrastructure.
 - The participant MUST ensure that the application is periodically tested for security vulnerabilities and ensure that there are no exploitable vulnerabilities are present.
 - The participant SHOULD not use any vulnerable third-party libraries. The participant MUST ensure that the application code is scanned for security vulnerabilities and there are no open exploitable issues.
 - The participant SHOULD ensure that its application does not re-use the same cryptographic keys for multiple purpose.
 - The participant SHOULD implement rate limiting measures to ensure not to overload the platform.
 - The participant SHOULD implement security auditing.


# Privacy Considerations

This section provides the privacy consideration for the DID method implementation.
 - No user personal data are stored on the registry.
 - The participant MUST ensure to protect integrity and confidentiality of user personal data. The participant MUST comply with all applicable privacy and data protection laws, regulations and principles.
 - The participant MUST ensure that there is no local storage of user personal data or any other sensitive information on a mobile device. If required, participant MUST ensure that necessary security controls are in place to protect user personal data.
 - The participant MUST ensure that no personal data is written on application log.
 - The participant MUST ensure that application does not store any personal data in temporary memory.
