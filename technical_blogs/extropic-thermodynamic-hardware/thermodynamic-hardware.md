## Main Issue

The main issue limiting current AI scaling is the **AI energy wall**. This demands unsustainable energy demands of current AI systems operating on traditional deterministic hardware.

Already, **almost every single new data center is experiencing difficulties sourcing power**. This thing went on some companies planned to power their own nuclear power plants on their own to get sustain in this AI scaling and met with energy requirements.

Because it **"would consume vastly more energy than humanity can produce"**.

So they extropic started working on the other side of the coin, which is **energy efficient computing hardware, algorithms for AI Scaling**.


![Energy](https://raw.githubusercontent.com/yeswanth49/blogs/main/technical_blogs/extropic-thermodynamic-hardware/images/person-ai-image.avif)

---
Main Question that may rise when reading about AI Scaling with energy efficiency.
#### Why Traditional CPUs/GPUs 
The main problem with these traditional CPUs or GPU is **communication waste** (consider, in CPUs and GPUs computations happen by transforming bits using logic and arithmetic operations, supported by these data movement between storage and processing units). Here the cost of communication is what causing this energy inefficiency (or some part of it, is responsible) - and this was not improved significantly over the last decade, nor it is expected to in the next decade.

Currently AI algorithms, designed to run well on GPUs (which are **"really bad at sampling"**), are inefficiently optimized around matrix multiplication in terms of AI scaling purposes.

---

### Extropic’s Breakthrough: Thermodynamic Computing
*(fascinating term in a while)*

Here Extropic Labs introduced a new computing hardware, algorithms, even some AI models, termed as **thermodynamic computing**.

Starting with **TSU (Thermodynamic Sampling Unit)** - optimized for the probabilistic sampling.  
Radically more energy efficient than traditional GPUs. Termed as **probabilistic hardware**.

![Hardware Image](https://raw.githubusercontent.com/yeswanth49/blogs/main/technical_blogs/extropic-thermodynamic-hardware/images/hardware-image.avif)

---

### Core Innovations

#### 1. **TSU (Thermodynamic Sampling Unit)**
These are new type of computing hardware. Which performs entirely different types of operation than CPUs and GPUs.  
Instead of processing a series of programmable deterministic computations, **TSUs produce samples from a programmable distribution**.

---

#### 2. **Probabilistic Circuits (Using Transistors)**
The concept of probabilistic circuits had existed in academia for decades, but designs were not commercially viable because they relied on exotic components that could not be built at scale using conventional transistor processes (like those from Intel or GlobalFoundries).  

Extropic invested years of effort into building models of the physics of transistors and developing new ways of understanding noise. This research enabled them to design new probabilistic circuits that use **only transistors**.

> **The X0 early test chip** was the hardware proof of technology designed to test these noise models and circuit designs. The successful experiments with X0 validated the design and proved that **all-transistor TSUs** could be built.

---

#### 3. **The pbit (Probabilistic Bit)**
This is the simplest circuit and a core component of first-generation TSUs.

- **Function**: It is a programmable analog hardware implementation of a **Bernoulli distribution** (a weighted coin flip), randomly switching between a '1' state (high level) and a '0' state (low level).  
- The probability of being in the '1' state is **arbitrarily programmable via a single input voltage**.

---

#### 4. **Denoising Thermodynamic Model (DTM)**
DTMs were inspired by diffusion models, and leverage TSUs to generate data by gradually pulling that data out of noise over several steps.  

You can find an explanation of how DTMs run on TSUs [here](https://extropic.ai/writing/tsu-101-an-entirely-new-type-of-computing-hardware).

> Running DTMs on our TSUs could be **10,000x more energy efficient** than modern algorithms running on GPUs, as shown by our simulations of TSUs running DTMs on the small benchmarks in [their paper](https://extropic.ai/).

---

### Software to Power the Hardware

**thrml library**  
The library that we used to write our simulations, [`thrml`](https://github.com/extropic-ai/thrml), is open sourced. Using `thrml` enables users to develop thermodynamic algorithms.

---

### The Future
And in future we might see **hybrid algorithms** which takes best of both worlds from TSUs and GPUs also.


## Read More 

[Blog](https://extropic.ai/writing/thermodynamic-computing-from-zero-to-one)