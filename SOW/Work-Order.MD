# AMD - NSF I/UCRC Consortium - Work Order

## NSF I/UCRC Consortium for Embedded Systems at Southern Illinois University Carbondale
The NSF Center for Embedded Systems (CES) is a research collaboration between academia (Southern Illinois University Carbondale and Arizona State University), Industry (leading embedded systems companies throughout the world) and government agencies (the National Science Foundation and other agencies). Its purpose is to advance in the field of embedded systems (hardware, software, and architectures) to new levels; thereby, sharing resulting advancements and commercializing applications in automotive, aerospace and micro-electronics to advance commerce.

**Contact:** Spyros Tragoudas, Professor & Department Chair, Electrical & Computer Engineering Department, SIUC

## AMD project summary

### Cascading Neural Network Models Application with a fused single kernel neural network model

**Duration:** 1 year

Develop an application which runs a lightweight model, which is optimized to use less power and resources, to detect some object or scene to trigger running of a more complex model, which does detection of a scene, bounding box, or segmentation, to complete a given task.

Considering this multi-layer cascading neural net model application, where the application relies on multiple neural network models. The first layer model, which is a small lightweight model, detects high-level hierarchy of object class and calls larger complex model to fine grain detect the object, the complex model may be shared for multiple applications in order to accommodate limited resources.

Use AMD hierarchical analysis and AMD experimental model scoring methodology in the development of models. A simple example application is detecting different breeds of dogs and cats, here the lightweight model detects if the animal in the image frame is a dog, it calls the complex model to detect the breed of the dog, else if the animal detected by the lightweight model is a cat, it calls the complex model to detect the breed of the cat.

The simple model should trigger the larger model when it detects some defined object or when the desired output is more complex than its specification. The assumption is that the common complex models will not be triggered on every frame in the application, hence multiple applications can run in real-time. A scheduler will handle collisions among different applications at the expense of a small increase in latency.

The smaller decision network is to be created as a fused single kernel network that handles all the optimizations within the kernel using existing AMD MIVisionX Libraries. AMD will provide access to training hardware on the cloud.

ADAT - AMD Data Analysis Toolkit, which is a part of MIVisionX can be used to verify models, ADAT could be updated to make changes required for application robustness.

All the results and studies need to be jointly published with AMD.

## Proposed Phases
### Quarter 1
Create a fused single kernel for the lightweight model in MIVisionX. Optimized for AMD hardware. The lightweight model will be designed to delegate certain tasks to a more complex model. Training this lightweight model can be done using transfer learning or trained using the ImageNet database. ADAT results to verify models and updates to ADAT pushed to MIVisionX.

### Quarter 2
Development of a lightweight model as in 1, for a second application. Start the development of the common larger model for the two applications. Update ADAT as required.

### Quarter 3
Profile the cascaded common model using AMD hardware, and make necessary adjustments for maximum saving in resources. Update ADAT as required.

### Quarter 4
Thorough experimental evaluation of proposed models. A study on applications other than vision/image that utilizes a simple lightweight model that feeds a common complex model that also handles the applications in 1 and 2. Comphrehensive ADAT results for the application.

## Budget:
$50K for a year.

**This will be an annual membership of AMD to the NSF IUCRC for Embedded Systems (CES). Matched by the NSF.**
