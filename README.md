# Artwork Custody DAML

This project uses DAML to model a multi-party custody chain for physical artowrks, and a fractional tokenisation mechanism for trading artwork derivatives on top of the actual artwork held in custody.

## Usage

This code is designed to run automatically from VS Code with the DAML plugin installed based on the docs here https://docs.daml.com/daml/intro/2_DamlScript.html. It can also be run from the command line using the `daml` cli tool. The testing script is at `Main:e2e_test_1`

## Business Context
Digitalization of artworks comes with a few particular problems.
* Many parties are required to guarantee and protect the value of an artwork for any investor
* A artwork can be very valuable and very small and mobile, therefore easily lost or stollen!
* Artworks can easily lose a lot of value if not stored correctly, damaged during transportation, or exposed to natural disasters, etc.
* The above issues traditionally exposes the investor to an investment diversification problem.

## Proposed Solution
Create a marketplace to which artworks can be taken into custody in atraceable way, and then traded as easy to invest token (ie: derivative). Combine the business partners (shipping, storage, art experts, custodian) into a chain of custody to protect owners and investors who thentrade tokens representing a fraction of the artwork. 

# Implementation Notes

## TO DO
1. fix wallet bugs
1. add proper unit tests
1. make code deployable

## Incomplete Business Implementation
1. block the underlying from changing state once it's been tokenised.
1. implement some form of fees to finance the custody process.
1. wallet has no protection around putting the same token twice.

## Notes
1. Had to move ensure from construction to creation choice time. Seems like I am weakening the model. Is there a different way?
1. is there better way to have default values or private constructors?
1. Is it possible to pass a ref/pointer to the latest contract record rather than instance of a record or an id/key?