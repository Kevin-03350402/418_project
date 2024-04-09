TITLE: 
Stellar Market Dynamics: Parallel Computing for Real-Time Multi-Asset Analysis

SUMMARY: 
We plan to design and implement a parallel computing system for real-time analysis of financial markets, focusing on regression and time series analysis across multiple assets. This system will leverage the computational capabilities of GPUs to simulate and predict market dynamics, akin to simulating celestial movements in a galaxy, by analyzing the internal trend of a certain asset (akin to celestial movement of a certain star) as well as the correlation among assets (similar to mutual gravity among stars).

BACKGROUND:
Our project aims to accelerate the compute-intensive application of financial market analysis. We would focus on regression and time series analysis across multiple assets. One important note to this application is the computation of mutual correlations between assets, which is similar to calculating gravitational forces in galaxy simulations. For instance, precious metals like gold, silver, platinum, and palladium often positively correlated and move in similar directions, while natural gas and coal tends to be negatively correlated as they can be substitutes for each other in power generation. The strength and even the direction of correlations are typically dynamic in the market. This aspect, along with internal data preprocessing and mathematical modeling, can benefit from parallelism due to the fact that the task can be distributed over multiple processing units. As the result, we expect promising significant speed enhancements for real-time market dynamics analysis and can be deployed into high-frequency trading


CHALLENGES:
The project aims to complete the challenging task of executing real-time financial market analysis with rapidly changing market data, where even minor delays could result in significant missed opportunities. The primary challenge lies in efficiently parallelizing the process, given the intricate nature of dependencies among assets and the necessity for high-speed data processing and analysis. Additionally, we need to make sure all the data that we used to conduct regression as well as quantifying the correlation are up-to-date, like the scenario where we have the keep track of a “recently updated” occupancy matrix in assignment 3 and 4. Hence, the core of the challenge lies in the intricacies of parallelizing computations that involve intricate dependencies among multiple assets. These dependencies create a complex web of interactions like the gravitational forces among celestial bodies in a galaxy.

The workload involved in this project is the need for rapid data ingestion and processing, where the memory access patterns can be irregular due to the varying nature of financial data streams. This irregularity brings concerns about memory locality and can lead to a high communication-to-computation ratio, particularly as the system scales to accommodate more assets and more detailed analysis. Such scaling can introduce divergent execution paths, as different assets may require different analytical approaches based on their historical data and market conditions. Therefore, data balancing can also be an important task. Additionally, we need to design reliable models to capture the trend of different assets and find a method to reasonably quantify the correlation among assets. 

A significant constraint in mapping this workload to a parallel computing system is the challenge of efficiently distributing tasks across multiple processors while minimizing overhead and making sure that data dependencies do not lead to bottlenecks or idle resources. This requires algorithms that can adaptively allocate resources based on the current state of the computation and the market. 

By undertaking this project, we aim to delve into the realms of parallel computing and financial analysis and develop a system capable of harnessing the power of modern GPUs. This system will not only need to manage the computational complexities of real-time data analysis but also ensure that the results are produced swiftly enough to be actionable. We expect it to overcome the inherent latency challenges and bring actual help to the users. 

RESOURCES:
We are planning to start from scratch. However, we will refer to external resources such as
academic paper.

GOALS
Main Goals (Plan to Achieve)
Objective 1: Develop a parallel model to conduct real-time simulation/prediction of the short-term performance of multiple assets utilizing asset attributes (its own historical data, seasonality, trend, etc.) as well as mutual correlations of different assets. We would rely on statistical methods to conduct quantitative analysis and conduct parameter optimization based on the dynamic data.
Stretch Goals (Hope to Achieve)
Objective 2: Enhance the performance of the model by incorporating not only identified correlations but also external economic indicators as well as market news. Additionally, we would like to introduce machine learning models for data processing, time series analysis, and support multimodality. The advancement in machine learning models and availability of high-quality economic data make this goal a little bit ambitious but yet achievable within the project timeframe.
Contingency Goals (If Behind Schedule)
Objective 3: If progress is slower than anticipated, focus on developing a robust model for a smaller subset of assets, such as a subgroup of correlated commodities. Concentrating on a narrower scope allows for a more detailed analysis and ensures that the project delivers valuable insights, even if it's on a smaller scale than initially planned. 

Demonstration Plan
Interactive Demo: At the poster session, we plan to present an interactive dashboard that visualizes the correlations and predictions made by our model. Users can select different commodities to see our real-time prediction as well as the actual performances of the assets.
Key Highlights: We will demonstrate the model's ability to simulate the fluctuations and correlations of multiple assets relatively accurately and showcase specific cases where the model successfully predicted price changes based on correlation analysis and external factors.
The project will deliver a parallel system to conduct reliable real-time simulations to support high-frequency trading based on short-term historical data. As a performance goal, we aim for the system to process updated commodity price data and refresh predictions on a millisecond basis, with a predictive accuracy rate that surpasses current benchmarks by at least 10%.

PLATFORM CHOICE:
1. Computer: Windows
2. Language: C/C++; Python
3. Mainly rely on Open MPI. The motivation is that Open MPI allows for detailed specification
of how computations are distributed across the GPU's cores. Additionally, it
provides various memory types and management techniques, allowing for optimized data
access patterns that can significantly reduce latency and increase throughput in compute intensive applications. Lastly, we are relatively familiar with Open MPI thanks to the training of HW3/4

SCHEDULE:
Week 1: Research and Planning
Conduct thorough research on parallel computing techniques suitable for financial market analysis.
Define project scope and establish clear benchmarks.
Week 2: Development Environment Setup
Set up the necessary development tools and environments for parallel computing (e.g., CUDA for NVIDIA GPUs).
Begin basic implementation of data ingestion modules.
Week 3: Core Algorithm Development
Develop the core algorithms for regression and time series analysis in parallel.
Start integrating algorithms with data ingestion modules.
Week 4: Optimization and Testing
Optimize algorithms for performance and efficiency.
Conduct initial testing on sample datasets to ensure accuracy and speed.
Week 5 (Milestone Week): Integration and Intermediate Testing
Integrate all components into a cohesive system.
Perform extensive testing and benchmarking to identify any bottlenecks or issues.
Prepare for presentation, summarizing progress and initial results.
