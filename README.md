# Artwork Custody DAML

This project uses DAML to model a multi-party custody chain for physical artowrks, and a fractional tokenisation mechanism for artworks in custody.

## Business Context
Digitalization of artworks comes with a few particular problems.
* Many parties are required to guarantee and protect the value of an artwork for any investor
* A artwork can be very valuable and very small and mobile, therefore easily lost or stollen!
* Artworks can easily lose a lot of value if not stored correctly, damaged during transportation, or exposed to natural disasters, etc.
* The above issues traditionally exposes the investor to an investment diversification problem.

## Proposed Solution
Create a marketplace to which artworks can be taken into custody in atraceable way, and then traded as easy to invest token (ie: derivative). Combine the business partners (shipping, storage, art experts, custodian) into a chain of custody to protect owners and investors who thentrade tokens representing a fraction of the artwork. 

## Questions
1. Is it possible to pass a ref/pointer to the latest contract record rather than instance of a record or an id/key?

## TO DO
1. fix wallet bugs
1. figure out how to use keys
1. figure out the issue with asserts
1. look at writing proper tests
1. run with inspector
1. clean up code
1. look at multi-party signing
1. is there better way to have default values or private constructors

## Incomplete Business Implementation
1. block the underlying from changing state once it's been tokenise.
1. implement some form of fees to finance the custody process.
1. wallet has no protection around putting the same token twice


## Notes
1. Had to move ensure from construction to creation choice time. Seems like I am weakening the model