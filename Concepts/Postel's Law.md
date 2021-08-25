#Concepts 
# Postel's Law (The Robustness Principle)

> Be conservative in what you do, be liberal in what you accept from others.

[[Technology Design]]

Often applied in server application development, this principle states that what you send to others should be as minimal and conformant as possible, but you should aim to allow non-conformant input if it can be processed.

The goal of this principle is to build systems which are robust, as they can handle poorly formed input if the intent can still be understood. However, there are potentially security implications of accepting malformed input, particularly if the processing of such input is not well tested. These implications and other issues are described by Eric Allman in [The Robustness Principle Reconsidered](https://queue.acm.org/detail.cfm?id=1999945).

Allowing non-conformant input, in time, may undermine the ability of protocols to evolve as implementors will eventually rely on this liberality to build their features.