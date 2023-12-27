# Target Solution for Amplitude Analytics

| Status        | Proposed |
:-------------- |:---------------------------------------------------- |
| **RFC #**     | [1.0](https://github.com/tensorflow/community/pull/NNN)|
| **Author(s)** | Agustina Leon (agustina.leon@productminds.io) |
| **Updated**   | 27-12-2023                                           |

## Objective

The goal of this project is for the users of Amplitude Analytics have the possibility to measure their target goals hourly, as they do not have it natively with the platform.

This project consists on developing an automated solution to upload the hourly goals per day with a CSV to be then sent to Amplitude. Each target goal will be sent as a new event (one per hour). For each event that we want to measure the target for, we must upload a new file with its targets.

## Motivation

GOL, a very important client of ours, came with the necessity of measuring these kind of targets as their daily ones could not capture in reality their changing sales rate through out the day. It is not the same the amount of flight tickets and hotels sold on a Sunday at 2PM than on the same day at 6PM.

If they keep on measuring the day as a whole they will keep on losing important insights and times of days where they could be improving.

Let's say we elevate this as a feature request to Amplitude, it could take a whole year for them to develop this. Plus, GOL will turn to other BI tools to do this and that is not what we want.

## User Benefit

How will users (or other contributors) benefit from this work? What would be the
headline in the release notes or blog post?

Measuring targets by hour in Amplitude, especially in businesses with high demand variability can help in:

- Efficient inventory management
- Resource allocation
- Optimizing performance

And thus, help teams reach their business top goals.

## Design Proposal

Below we will present the C4 diagram of the solution presenting each of the components and technologies involved in the architecture.


[C4 DIAGRAM]


### Alternatives Considered
* Make sure to discuss the relative merits of alternatives to your proposal.

### Implications
* Do you expect any (speed / memory)? How will you confirm?
* There should be microbenchmarks. Are there?
* There should be end-to-end tests and benchmarks. If there are not (since this is still a design), how will you track that these will be created?


### Tutorials and Examples
* If design changes existing API or creates new ones, the design owner should create end-to-end examples (ideally, a tutorial) which reflects how new feature will be used. Some things to consider related to the tutorial:
    - The minimum requirements for this are to consider how this would be used in a Keras-based workflow, as well as a non-Keras (low-level) workflow. If either isn’t applicable, explain why.
    - It should show the usage of the new feature in an end to end example (from data reading to serving, if applicable). Many new features have unexpected effects in parts far away from the place of change that can be found by running through an end-to-end example. TFX [Examples](https://github.com/tensorflow/tfx/tree/master/tfx/examples) have historically been good in identifying such unexpected side-effects and are as such one recommended path for testing things end-to-end.
    - This should be written as if it is documentation of the new feature, i.e., consumable by a user, not a TensorFlow developer. 
    - The code does not need to work (since the feature is not implemented yet) but the expectation is that the code does work before the feature can be merged. 


## Questions and Discussion Topics

Seed this with open questions you require feedback on from the RFC process.