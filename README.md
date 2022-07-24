# ECDSA secpr1 Data Integrity Cryptosuite

This specification describes a Data Integrity Cryptosuite for use when generating a Elliptic Curve Digital Signature Algorithm (ECDSA) based on the Standards for Efficient Cryptography over Prime fields using the R1 Elliptic Curve (secpr1). The approach is accepted by the U.S. National Institute of Standards and meets U.S. Federal Information Processing requirements when using cryptography to secure digital information.

The specification defining the cryptography suite is available at the following URL: [https://w3c-ccg.github.io/di-ecdsa-nist-2019/](https://w3c-ccg.github.io/di-ecdsa-nist-2019/)

## Implementations

- none so far

## Abstract

Just like the exiting CCG work items for the <a
href="https://w3c-ccg.github.io/di-eddsa-2022/">Ed25519 Cryptosuite</a>, the <a href="https://w3c-ccg.github.io/lds-ecdsa-secp256k1-2019/">Secp256k1 Cryptosuite</a>, and the <a href="https://w3c-ccg.github.io/ldp-bbs2020/">BBS+ Cryptosuite</a>, this cryptosuite extends the Data Integrity specification to support cryptography supported by many large organizations and governments throughout the world.

## Owners

Owners: @msporny, @martyr280

## Work Item Questions

> 1. Explain what you are trying to do using no jargon or acronyms.

This specification adds support for a type of digital signature that is used heavily by large organizations throughout the world. It was our hope that we would not have to support this digital signature suite due to it's <a href="https://crypto.stackexchange.com/questions/10263/should-we-trust-the-nist-recommended-ecc-parameters">controversial nature</a>, but given the slow pace of the hardware security module industry, along with the slow pace at which national institutes that standardize cryptography are moving, and given the hostility of a vocal minority of W3C Member companies towards the scope of the Verifiable Credentials work, publishing this work item and folding it into the VCWG 2.0 work protects that work from any W3C Member that might insist that work on this technology is out of scope (and thus hobbling the VCWG group's ability to be responsive to cryptographic needs in the industry).

> 2. How is it done today, and what are the limits of the current practice?

The current focus of Elliptic Curve digital signatures in the VC ecosystem seems to be around something called the "Twisted Edwards Curve", or Ed25519. That cryptography uses provably secure techniques. Unfortunately, that technology has just been approved by the National Institute of Standards in draft form and it might take years for it to be supported in the commercial hardware security modules that many governments and large organizations depend on. It was our hope that the industry was going to make more progress by this point, but it's not moving fast enough. We plan to standardize a few cryptosuites in the upcoming VCWG 2.0 work. In order to mitigate the risk that Ed25519 won't be available in commercial hardware security modules by the time that some vendors need to deploy into production settings with large organizations and governments, we are suggesting that ECDSA Secpr1 should be an option for Issuers that desire its functionality.

> 3. What is new in your approach and why do you think it will be successful?

There is nothing new in the approach, in fact, the cryptography used here is fairly old (almost 20+ years at this point). If it is successful, it will be because of the broad market adoption that the technology already has.

> 4. How are you involving participants from multiple skill sets and global locations in this work item? (Skill sets: technical, design, product, marketing, anthropological, and UX. Global locations: the Americas, APAC, Europe, Middle East.)

Due to the nature of the work item (cryptographic security), it is difficult to include non-technical participants. We will be involving the CCG and VCWG, which do include non-technical participants throughout the world, but again, their ability to influence the technical direction will be quite limited.

> 5. What actions are you taking to make this work item accessible to a non-technical audience?

Overall, none, as non-technical audiences need not be exposed to this level of detail.

We will happily try and explain what we're doing on the CCG mailing list if non-technical members have questions about the technology.
