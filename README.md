# Integrate `Arbitrary Contract Interaction` into baseDAO

## Description of the task
The goal is to produce a piece of Michelson code which will be used as parameter in a call to the [baseDAO contract](https://github.com/tezos-commons/baseDAO/) on the `propose` endpoint to extend the functionality of the contract.
In the context of baseDAO, Lambdas are pieces of code that define specific types of proposals. The contract comes with some default Lambdas (such as `transfer`, `change_config`, `set_delegate`) and it also allows adding more.
We are after the Lambda code pertaining to an Arbitrary Contract Interaction capability. Once approved through the normal proposal flow, this would allow the baseDAO contract to call any endpoint on another deployed contract in the same way an individual user can do so from their wallet.


## Supporting materials
- **UI flow**: To get a better sense of the desired outcome from a user perspective, check out this [UI flow](https://xd.adobe.com/view/27f6cc79-2bbb-4f70-85fa-7f2b1fbfefc5-72a5/?fullscreen)
- **Past work**: [This SO thread](https://stackoverflow.com/questions/78896531/michelson-parsing-error-in-proposal-handler-integration/78964599#78964599) details the findings from a few attempts made using different tools.
- **TZ Safe** already have implemented this functionality in their contract: https://github.com/marigold-dev/tzsafe/blob/release-0.3/test/test_lambda_proposal.mligo


## Definition of done
1. The delivered code should pass the [validation](https://github.com/tezos-commons/baseDAO/blob/be77424a313ace8e3f3c2748a1cbbc18acfe8001/src/variants/lambda/types.mligo#L63) done by the baseDAO contract.

2. The delivered code should contain the logic for relaying a contract call based on provided data. The success or failure of the final execution of  is outside of the scope of this task, and we are not necessarily looking to integrate a transaction simulation at this stage. But assuming that the call is allowed by the logic of the destination contract, it should go through successfully. To that end, for the purposes of establishing successful completion of this task, we should use a very simple contract on Ghostnet, with an endpoint that just changes the value of a string.

3. The delivered code should come with some minimal documentation or code comments to ensure maintainability.

The contractor should submit their work to the `submissions` folder.


###  Payment Terms and Duration

- **Maximum Duration**: The Contractor must be completed within 3 months after signing this Project on the Trustless Business platform. 

- **Amount**: XTZ equivalent of $2000. Conversion rate is applied at the time when the contract is signed and the tokens are locked in escrow as per the operating model of Trustless Business
- **Payment Timing **: One month after successful delivery and acceptance of the completed project.

- **Extension Policy**: Short extensions can be discussed and may be permitted based on invoked circumstances.
- **Maximum Extension**: Total extension time not to exceed 4 weeks.

## Dispute Resolution
In case of disputes, this file and contents of the `submissions` folder serve as the primary reference points. The designated arbiter will use these documents to resolve any disagreements.


