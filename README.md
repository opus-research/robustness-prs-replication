# On the Investigation of Exception Pull Request Characteristics: Exploring the Apache Ecosystem

Robustness is critical for ensuring that software functions correctly under adverse conditions. Exception-handling mechanisms in programming languages enable developers to structure the code that deals with these adverse conditions. However, implementing the exception-related code may present significant challenges to developers. In this context, this paper reports a study in which we investigated the attention given by developers to the exception-related code across Java projects of the Apache ecosystem. We analyzed the exception-related pull requests (exception-PRs), which were detected with a validated heuristic, to characterize and classify the aspects of these contributions. We produced a comprehensive dataset of 986 exception-PRs detected with the proposed heuristic. A tally of 280 PRs was manually analyzed to characterize and classify the aspects of these contributions to the exception-related code. Our results reveal several trends. First, no statistically significant differences are observed in complexity metrics for exception-PRs versus non-exception-PRs. Similarly, no significant differences are observed in developers' behavior metrics, indicating consistent engagement regardless of whether the pull request addressed exceptional code or not. Most exception-PRs focus on system improvements rather than bug fixes, underscoring proactive efforts to enhance software robustness. Moreover, the most frequently addressed aspects of exceptional code in these exception-PRs are: (i) the external representation of the adverse situations to end-users (more than 40\% of the PRs), and (ii) the implementation of effective error handling actions (nearly 35\% of the PRs) to promote the program recoverability. Interestingly, a significant proportion of exception-PRs addresses simultaneously various of these (and other) aspects.

# RQ1: How does the dynamics of exception-PRs and non-exception-PRs differ? 

### Artifacts
- [Full list of exception-PRs identified by the heuristic in the Druid.](exception-PRs-druid.pdf)
- [Full list of exception-PRs identified by the heuristic in the Pulsar.](exception-PRs-pulsar.pdf)
- [Full list of exception-PRs identified by the heuristic in the Flink.](exception-PRs-flink.pdf)

# RQ2: What are the aspects addressed by exception-PRs?
### Artifacts

- [Full list of exception-PRs and answers from manual validation.](exception-PRs-manual-validation.pdf) 

### Full tables
| Exception aspect occurrence                    | %      | #  | Bug fix | Improvement | New feature | Test  | Other |
|------------------------------------------------|--------|----|---------|-------------|-------------|-------|-------|
| Error representability - External              | 42.52% | 108| 19.44%  | 77.77%      | 1.85%       | 0.92% | 0.00% |
| Error recoverability - Effective error handling| 36.22% | 92 | 48.91%  | 46.73%      | 2.17%       | 1.08% | 1.08% |
| Error detectability                            | 23.62% | 60 | 40.00%  | 56.67%      | 0.00%       | 3.33% | 0.00% |
| Error representability - Internal              | 20.47% | 52 | 36.53%  | 63.46%      | 0.00%       | 0.00% | 0.00% |
| Error recoverability - Program continuity      | 20.47% | 52 | 55.76%  | 42.30%      | 0.00%       | 1.92% | 0.00% |
| Other                                          | 19.69% | 50 | 68.00%  | 26.00%      | 0.00%       | 6.00% | 0.00% |
| Error propagartion                             | 16.54% | 42 | 26.19%  | 69.05%      | 2.38%       | 2.38% | 0.00% |
| Error recoverability - Cleanability            | 7.48%  | 19 | 36.84%  | 63.15%      | 0.00%       | 0.00% | 0.00% |

<h5 align="center">Table VI: Exception aspects and the aim of the contribution in exception-PRs</h5>

| Exception aspect occurrence (combinations)                                   | %      | #  | Bug fix | Improvement | New feature | Test | Other |
|------------------------------------------------------------------------------|--------|----|---------|-------------|-------------|------|-------|
| Error recoverability, Error representability                                 | 12.99% | 33 | 39.39%  | 57.58%      | 3.03%       | 0.00%| 0.00% |
| Error detectability, Error recoverability, Error representability           | 7.09%  | 18 | 44.44%  | 55.56%      | 0.00%       | 0.00%| 0.00% |
| Error propagartion, Error recoverability, Error representability            | 5.51%  | 14 | 42.86%  | 50.00%      | 7.14%       | 0.00%| 0.00% |
| Error detectability, Error representability                                  | 4.33%  | 11 | 18.18%  | 81.82%      | 0.00%       | 0.00%| 0.00% |
| Error detectability, Error recoverability                                    | 3.94%  | 10 | 70.00%  | 30.00%      | 0.00%       | 0.00%| 0.00% |
| Error propagartion, Error representability                                   | 3.94%  | 10 | 10.00%  | 90.00%      | 0.00%       | 0.00%| 0.00% |
| Error detectability, Error propagartion, Error recoverability               | 1.57%  | 4  | 25.00%  | 75.00%      | 0.00%       | 0.00%| 0.00% |
| Error propagartion, Error recoverability                                     | 1.18%  | 3  | 33.33%  | 66.67%      | 0.00%       | 0.00%| 0.00% |
| Error detectability, Error propagartion, Error representability             | 0.79%  | 2  | 0.00%   | 100.00%     | 0.00%       | 0.00%| 0.00% |
| Error recoverability, Other                                                 | 0.79%  | 2  | 50.00%  | 50.00%      | 0.00%       | 0.00%| 0.00% |
| Error propagartion, Other                                                   | 0.39%  | 1  | 0.00%   | 100.00%     | 0.00%       | 0.00%| 0.00% |
| Error detectability, Error recoverability, Other                            | 0.39%  | 1  | 100.00% | 0.00%       | 0.00%       | 0.00%| 0.00% |
| Error propagartion, Error representability, Other                           | 0.39%  | 1  | 0.00%   | 100.00%     | 0.00%       | 0.00%| 0.00% |
| Error representability, Other                                               | 0.39%  | 1  | 0.00%   | 100.00%     | 0.00%       | 0.00%| 0.00% |


<h5 align="center"> Table VII: Combination of exception aspects and the aim of contribution in exception-PRs.</h5>