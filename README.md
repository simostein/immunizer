This is a proof of concept Java implementation of our Framework for Immune Applications through Application-level Unsupervised Outlier-based Intrusion Detection and Prevention.

**Dependencies**
- OpenJDK 10: mainly to support ByteBuddy
- ByteBuddy 1.8.3: to instrument applications at runtime 
- Gson 2.8.5: to generate JSON trees out of invocation parameters and returned values
- ELKI 0.7: to apply several outlier detection algorithms and distance functions

**Structure**
- apps: applications to which we apply our framework through instrumentation
- evaluation: outlier detection evaluation, currently based on R-precision
- framework: our framework implementation
- models: folder to host models generated by our framework for each immunized/instrumented application