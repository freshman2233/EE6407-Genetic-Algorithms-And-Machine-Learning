# EE6407 Genetic Algorithms And Machine Learning

**语言**

[English](./README.md)     [中文](./README_CN.md)

# 1.Introduction

This course, **EE6407 - Genetic Algorithms and Machine Learning**, offers an integrated view of these two complementary domains. 

The first half of the course delves into **evolutionary algorithms**—their design, implementation, and applications in complex optimization tasks—while the second half provides a comprehensive introduction to **machine learning** paradigms, equipping students with the latest theoretical foundations and practical approaches to contemporary ML challenges. 

By blending these topics, the course ensures a holistic understanding of how to address diverse computational problems through both optimization and learning strategies, setting the stage for advanced applications and further research in this rapidly evolving field.

This repository serves as a comprehensive resource for students and enthusiasts alike. 

1. **Personal Solutions to Past Exams** – Detailed, step-by-step write-ups of previously tested questions to guide your revision and deepen conceptual understanding.
2. **PPT Example References** – Walkthroughs of example problems and exercises presented in the lecture slides, clarifying key ideas and methodologies.
3. **Analysis of Challenging Topics** – In-depth discussions and breakdowns of complex areas, helping you navigate common pitfalls and master advanced concepts.

If you happen to have a GitHub account and find this repository helpful, please consider giving it a star⭐.

![3b54fe6d9ee63d988dc3834460c147b](./README.assets/3b54fe6d9ee63d988dc3834460c147b.jpg)

# 2.OBJECTIVE

The objective of first half of this course is to provide in-depth treatment on **optimization** procedures based on **evolutionary algorithms**. As most modern optimization problems are complex with mixed real-integer variables, numerous locally optimal solutions, discontinuities, and so on. Evolutionary algorithms can handle all these issues more effectively than other optimization algorithms.

The objective of second half of this course is to equip students with **machine learning** theories and paradigms. It gives the students an understanding of the most current machine learning algorithms such as **deep learning, kernel methods**, **randomization-based** methods so that the students can apply the knowledge to **data mining, pattern recognition and regression problems.**

# 3.CONTENT

Review of Combinatorics and Probability. 

Introduction of Genetic Algorithms.

Differential Evolution. 

Particle Swarm Optimization. 

Advanced Techniques. 

Principles of Machine Learning. 

Paradigms of Machine Learning. 

Kernel Methods.

# 4.**REFERENCES**

1. Christopher M. Bishop, Pattern Recognition and Machine Learning, Springer, 2016 (Latest Edition).

2. Trevor Hastie, Robert Tibshirani, Jerome Friedman, The Elements of Statistical Learning (Springer Series in Statistics), 9th printing, 2017.

3. Andries P. Engelbrecht, Computational Intelligence: An Introduction, Wiley, 2007

# 5.Content

5.1GeneticAlgorithms

1.ProblemstoBeSolved

1.1"BlackBox"Model
1.1.1Optimization
1.1.2Modeling
1.1.3Simulation

1.2SearchProblems

1.3Optimizationvs.ConstraintSatisfaction
1.3.1ObjectiveFunction
1.3.2Constraints
1.3.3COP(ConstraintOptimizationProblem)
1.3.4CSP(ConstraintSatisfactionProblem)
1.3.5FOP(FreeOptimizationProblem)
1.3.6NoProblem

1.4NPProblems
1.4.1KeyConcepts
1.4.2ClassesP,NP,NPcomplete,andNPhard
1.4.3DifferencesBetweenClasses

2.EvolutionaryComputation:Origins

2.1HistoricalPerspective
2.2BiologicalInspiration
2.2.1DarwinianEvolution
2.2.2Genetics

2.3SummaryofEvolutionaryComputationMetaphors

3.WhatAreEvolutionaryAlgorithms?

3.1EvolutionaryAlgorithmFramework
3.1.1GeneralEvolutionaryAlgorithmFramework
3.1.2PseudocodeofEvolutionaryAlgorithm
3.1.3GeneralModeloftheEvolutionaryProcess
3.1.4TwoPillarsofEvolution

3.2MajorComponentsofEvolutionaryAlgorithms
3.2.1Representation
3.2.1.1Roles
3.2.1.2Genotype
3.2.1.3Phenotype
3.2.1.4Encoding
3.2.1.5Decoding
3.2.1.6Example:RepresentingIntegerValueswithBinaryCode
3.2.2Evaluation(Fitness)Function
3.2.3Population
3.2.4SelectionMechanism
3.2.5VariationOperators
3.2.6Mutation
3.2.7Recombination
3.2.8Initialization/Termination
3.2.9DifferentTypesofEvolutionaryAlgorithms

3.3Example:The8QueensProblem
3.3.1Representation
3.3.1.1Phenotype
3.3.1.2Genotype
3.3.2FitnessEvaluation
3.3.3Mutation
3.3.4Recombination

3.4Example:\(f(x)=x^2\)
3.5TypicalEvolutionaryAlgorithmBehavior
3.6EvolutionaryComputationandGlobalOptimization
3.7EvolutionaryComputationandCommunitySearch

4.Representation,Mutation,andRecombination

4.1EvolutionaryAlgorithmFramework:GeneralEvolutionaryAlgorithmFramework
4.2RoleofRepresentationandVariationOperators

4.3BinaryRepresentation
4.3.1Mutation
4.3.2OnePointCrossover
4.3.3AlternativeCrossoverOperators
4.3.4nPointCrossover
4.3.5UniformCrossover
4.3.6CrossoverorMutation?

4.4IntegerRepresentation
4.5RealValuedorFloatingPointRepresentation
4.5.1MappingRealNumbersontoBitStrings
4.5.2UniformMutation
4.5.3NonUniformMutation
4.5.4AdaptiveMutation
4.5.5CrossoverOperators
4.5.6SingleArithmeticCrossover
4.5.7SimpleArithmeticCrossover
4.5.8WholeArithmeticCrossover
4.5.9BlendCrossover
4.5.10OverviewofDifferentPossibleOffspring
4.5.11MultiParentRecombination
4.5.12MultiParentRecombinationType1
4.5.13MultiParentRecombinationType2

4.6PermutationRepresentation
4.6.1TSPExample
4.6.2Mutation
4.6.3SwapMutation
4.6.4InsertionMutation
4.6.5ScrambleMutation
4.6.6InversionMutation
4.6.7CrossoverOperators
4.6.8Order1Crossover
4.6.9PartiallyMappedCrossover(PMX)
4.6.10CycleCrossover
4.6.11EdgeRecombination
4.7TreeRepresentation

5.Fitness,Selection,andPopulationManagement

5.1GeneralEvolutionaryAlgorithmFramework
5.2PopulationManagementModels:Introduction

5.3ParentSelection
5.3.1FitnessProportionalSelection
5.3.1.1WindowedScaling
5.3.1.2SigmaScaling

5.4RankBasedSelection
5.4.1LinearRanking
5.4.2ExponentialRanking

5.5ParentSelection
5.5.1TournamentSelection

5.6UniformParentSelection
5.7SurvivorSelection
5.8FitnessBasedReplacement
5.9SelectionPressure



5.2MachineLearning

1.ArtificialIntelligence,MachineLearning,NeuralNetworks,andDeepLearning:Overview

1.1IntroductiontoMachineLearning

1.2WhatisHumanLearning?
1.2.1TypesofHumanLearning
1.2.1.1LearningUnderExpertGuidance
1.2.1.2LearningGuidedbyExpertKnowledge
1.2.1.3LearningThroughSelfStudy

1.3WhatisMachineLearning?
1.3.1HowDoMachinesLearn?
1.3.1.1Abstraction
1.3.1.2Induction

1.4TypesofMachineLearning
1.4.1SupervisedLearning
1.4.1.1Classification
1.4.1.2Regression
1.4.2UnsupervisedLearning
1.4.3ReinforcementLearning

1.5ApplicationsofMachineLearning
1.5.1BankingandFinance
1.5.2Insurance
1.5.3Healthcare

1.6AdvancedLanguages/ToolsinMachineLearning
1.6.1Python
1.6.2R
1.6.3MATLAB

1.7MachineLearningChallenges
1.8Summary

2.MachineLearningDataPreparation

2.1MachineLearningActivities
2.2FundamentalDataTypesinMachineLearning
2.3ExploringDataStructures
2.4ExploringNumericalData
2.4.1UnderstandingCentralTendency
2.4.2UnderstandingDataDistribution
2.4.2.1MeasuringDataDispersion
2.4.2.2MeasuringDataValuePosition
2.4.3PlottingandExploringNumericalData
2.4.3.1Boxplots
2.4.3.2Histograms

2.5ExploringCategoricalData
2.6ExploringRelationshipsBetweenVariables
2.6.1ScatterPlots
2.6.2ContingencyTables

2.7DataQualityandCleaning
2.7.1DataQuality
2.7.2DataCleaning
2.7.2.1HandlingOutliers
2.7.2.2HandlingMissingValues

2.8DataPreprocessing
2.8.1FeatureScaling
2.8.2Normalization
2.8.3Standardization
2.8.4DimensionalityReduction

2.9Summary



3.BayesianDecisionTheory

3.1PriorProbability

3.2PosteriorProbability

3.3BayesianDecisionRule

3.4JointProbability

3.5UnivariateNormalDensityFunction

3.6MultivariateNormalDensityFunction

3.7ParameterEstimationforGaussianDensityFunction

3.8MaximumLikelihoodParameterEstimation
3.8.1LikelihoodFunction
3.8.2LogLikelihoodFunction
3.8.3NecessaryConditionsforMaximumLikelihoodEstimation
3.8.4MaximumLikelihoodEstimation(MLE)
3.8.5MLEfor\(\mu\)and\(\Sigma\)
3.8.6Example

3.9GaussianMixtureModel(GMM)
3.9.1NormalDistribution
3.9.2ParameterEstimation

3.10ExpectationMaximization(EM)
3.10.1Algorithm
3.10.2GMM+EM
3.10.3Example2

3.11NaïveBayes
3.11.1JointProbability
3.11.2PosteriorProbability
3.11.3TypesofClassifiers
3.11.3.1GaussianNaïveBayes
3.11.3.2BernoulliNaïveBayes
3.11.3.3MultinomialNaïveBayes
3.11.3.3.1LaplaceSmoothing(AddOneMethod)







# 6.List of Github

`````
D:.
│  .gitattributes
│  .gitignore
│  LICENSE
│  list.txt
│  README.md
│  README_CN.md
│  
├─1.Exam
│      .keep
│      22-S2-Q1.pdf
│      23-S1-Q1.pdf
│      23-S2-Q1.pdf
│      24-S1-Q1.pdf
│      
├─2.PPT Example
│  ├─1.GA
│  │      1.4.2 Eight-Queen-v2.pdf
│  │      1.4.2 P、NP、NP-complete 和 NP-hard 类 举例-V2.pdf
│  │      1.4.2 P、NP、NP-complete 和 NP-hard 类 举例.pdf
│  │      1.4.2 TSP belong to NP-complete.pdf
│  │      3 2.5 Example understand.pdf
│  │      3.3 The 8-queens problem Recombination.pdf
│  │      3.3.4-Eight-Queens-Recombination.pdf
│  │      3.4 EC & neighbourhood search.pdf
│  │      3.4 SGA EXAMPLE f(x) = x^2.pdf
│  │      4.5.1 mapping read values on bit string.pdf
│  │      4.6.10 循环交叉.pdf
│  │      4.6.11边缘重组-v2.pdf
│  │      4.6.8顺序1阶交叉.pdf
│  │      4.6.9 部分映射交叉(PMX) EXAMPLE1.pdf
│  │      4.6.9 部分映射交叉(PMX) EXAMPLE2.pdf
│  │      4.6.9 部分映射交叉(PMX) PPT.pdf
│  │      4.7 Tree Representation.pdf
│  │      5.4.1 Linear Ranking.pdf
│  │      5.4.2 Exponential Ranking.pdf
│  │      5.5.1 Tournament selection-with replacement-P smaller than 1.pdf
│  │      5.5.1 Tournament selection-without replacement-P equal 1.pdf
│  │      5.9 Selection pressure.pdf
│  │      
│  └─2.ML
│          2.4.2.1 data dispersion.pdf
│          2.4.3.1 Box plots.pdf
│          
├─3.Understand
│      .keep
│      1.1Example of Branch and bound 分支定界.pdf
│      1.2Example of simulated annealing模拟退火.pdf
│      1.Metaheuristics 元启发式方法VS Deterministic Algorithm确定性方法.pdf
│      2.TSP.pdf
│      3.NP problem.pdf
│      4.P NP NP-complete NP-hard Example-V3.pdf
│      5.Eight Queens.pdf
│      6.GA-v2.pdf
│      7.No Free Lunch in optimization.pdf
│      
├─4.Resource
│  ├─1.OUTLINE
│  │      EE6407-OUTLINE.pdf
│  │      
│  ├─2.EXAM-SUMMARY-CN
│  │      6407考试原题.docx
│  │      
│  └─3.REFERENCES
│          Computational Intelligence. An Introduction (Andries P. Engelbrecht) (Z-Library).pdf
│          Introduction-To-Evolutionary-Computing.pdf
│          Pattern Recognition and Machine Learning (Christopher M. Bishop) (Z-Library).pdf
│          The Elements of Statistical Learning Data Mining, Inference, and Prediction (2nd edition) (12print 2017) (Trevor Hastie, Robert Tibshirani etc.) (Z-Library).pdf
│          遗传算法-基本术语(中英文对照).pdf
│          
├─assets
│      3b54fe6d9ee63d988dc3834460c147b.jpg
│      
└─README.assets
        3b54fe6d9ee63d988dc3834460c147b.jpg
        

`````



# 7.Disclaimer

All content in this  is based solely on the contributors' personal work, Internet data.
All tips are for reference only and are not guaranteed to be 100% correct.
If you have any questions, please submit an Issue or PR.
In addition, if it infringes your copyright, please contact us to delete it, thank you.



#### Copyright © School of Electrical & Electronic Engineering, Nanyang Technological University. All rights reserved.
