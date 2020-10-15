# Adversarial Explainable AI

A curated list of Adversarial Explainable AI (XAI) resources, inspired by
[awesome-adversarial-machine-learning](https://github.com/yenchenlin/awesome-adversarial-machine-learning) and
[awesome-interpretable-machine-learning](https://github.com/lopusz/awesome-interpretable-machine-learning).
Due to the novelty of the field, this list is very much in the making. Contributions are welcome - send a pull request
or contact me [@hbaniecki](https://github.com/hbaniecki#:~:text=hbaniecki@gmail.com).

<p align="center"><img src="fig/aiml.png"></p>

There are various adversarial attacks on machine learning models; hence, ways of defending, e.g. by using XAI techniques. Nowadays, attacks on model explanations come to light, so does the defense to such adversary. 

<p align="center"> <em>Veritas Vincit</em> </p>

## Papers

### General

* [Towards Robust Interpretability with Self-Explaining Neural Networks](https://papers.nips.cc/paper/8003-towards-robust-interpretability-with-self-explaining-neural-networks#:~:text=pdf)
  <details>
  <summary> D. A. Melis & T. Jaakkola <em>Advances in Neural Information Processing Systems</em> 2018 </summary>
    Most recent work on interpretability of complex machine learning models has focused on estimating a-posteriori explanations for previously trained models around specific predictions. Self-explaining models where interpretability plays a key role already during learning have received much less attention. We propose three desiderata for explanations in general -- explicitness, faithfulness, and stability -- and show that existing methods do not satisfy them. In response, we design self-explaining models in stages, progressively generalizing linear classifiers to complex yet architecturally explicit models. Faithfulness and stability are enforced via regularization specifically tailored to such models. Experimental results across various benchmark datasets show that our framework offers a promising direction for reconciling model complexity and interpretability.
  </details>
* [Sanity Checks for Saliency Maps](https://papers.nips.cc/paper/8160-sanity-checks-for-saliency-maps#:~:text=pdf#:~:text=pdf)
  <details>
  <summary> A. Julius et al. <em>Advances in Neural Information Processing Systems</em> 2018 </summary>
    Saliency methods have emerged as a popular tool to highlight features in an input deemed relevant for the prediction of a learned model. Several saliency methods have been proposed, often guided by visual appeal on image data. In this work, we propose an actionable methodology to evaluate what kinds of explanations a given method can and cannot provide. We find that reliance, solely, on visual assessment can be misleading. Through extensive experiments we show that some existing saliency methods are independent both of the model and of the data generating process. Consequently, methods that fail the proposed tests are inadequate for tasks that are sensitive to either data or model, such as, finding outliers in the data, explaining the relationship between inputs and outputs that the model learned, and debugging the model. We interpret our findings through an analogy with edge detection in images, a technique that requires neither training data nor model. Theory in the case of a linear model and a single-layer convolutional neural network supports our experimental findings.
  </details>
* [On Relating Explanations and Adversarial Examples](https://papers.nips.cc/paper/9717-on-relating-explanations-and-adversarial-examples#:~:text=pdf)
  <details>
  <summary> A. Ignatiev et al. <em>Advances in Neural Information Processing Systems</em> 2019 </summary>
    The importance of explanations (XP's) of machine learning (ML) model predictions and of adversarial examples (AE's) cannot be overstated, with both arguably being essential for the practical success of ML in different settings. There has been recent work on understanding and assessing the relationship between XP's and AE's. However, such work has been mostly experimental and a sound theoretical relationship has been elusive. This paper demonstrates that explanations and adversarial examples are related by a generalized form of hitting set duality, which extends earlier work on hitting set duality observed in model-based diagnosis and knowledge compilation. Furthermore, the paper proposes algorithms, which enable computing adversarial examples from explanations and vice-versa.
  </details>
* [Robustness in Machine Learning Explanations: Does It Matter?](https://www.dropbox.com/s/u4kwdk9m5o2u2sb/preprint.pdf)
  <details>
  <summary> H. L. Leif <em>Conference on Fairness, Accountability, and Transparency</em> 2020 </summary>
    The explainable AI literature contains multiple notions of what an explanation is and what desiderata explanations should satisfy. One implicit source of disagreement is how far the explanations should reflect real patterns in the data or the world. This disagreement underlies debates about other desiderata, such as how robust explanations are to slight perturbations in the input data. I argue that robustness is desirable to the extent that we’re concerned about finding real patterns in the world. The import of real patterns differs according to the problem context. In some contexts, non-robust explanations can constitute a moral hazard. By being clear about the extent to which we care about capturing real patterns, we can also determine whether the Rashomon Effect is a boon or a bane.
  </details>

### Attack

* [Interpretation of Neural Networks Is Fragile](https://www.aaai.org/ojs/index.php/AAAI/article/view/4252#:~:text=pdf)
  <details>
  <summary> A. Ghorbani et al. <em>AAAI Conference on Artificial Intelligence</em> 2019 </summary>
  In order for machine learning to be trusted in many applications, it is critical to be able to reliably explain why the machine learning algorithm makes certain predictions. For this reason, a variety of methods have been developed recently to interpret neural network predictions by providing, for example, feature importance maps. For both scientific robustness and security reasons, it is important to know to what extent can the interpretations be altered by small systematic perturbations to the input data, which might be generated by adversaries or by measurement biases. In this paper, we demonstrate how to generate adversarial perturbations that produce perceptively indistinguishable inputs that are assigned the same predicted label, yet have very different interpretations. We systematically characterize the robustness of interpretations generated by several widely-used feature importance interpretation methods (feature importance maps, integrated gradients, and DeepLIFT) on ImageNet and CIFAR-10. In all cases, our experiments show that systematic perturbations can lead to dramatically different interpretations without changing the label. We extend these results to show that interpretations based on exemplars (e.g. influence functions) are similarly susceptible to adversarial attack. Our analysis of the geometry of the Hessian matrix gives insight on why robustness is a general challenge to current interpretation approaches.
  </details>
* [Fairwashing: the risk of rationalization](http://proceedings.mlr.press/v97/aivodji19a#:~:text=pdf)
  <details>
  <summary> U. Aivodji et al. <em>International Conference on Machine Learning</em> 2019 </summary>
  Black-box explanation is the problem of explaining how a machine learning model – whose internal logic is hidden to the auditor and generally complex – produces its outcomes. Current approaches for solving this problem include model explanation, outcome explanation as well as model inspection. While these techniques can be beneficial by providing interpretability, they can be used in a negative manner to perform fairwashing, which we define as promoting the false perception that a machine learning model respects some ethical values. In particular, we demonstrate that it is possible to systematically rationalize decisions taken by an unfair black-box model using the model explanation as well as the outcome explanation approaches with a given fairness metric. Our solution, LaundryML, is based on a regularized rule list enumeration algorithm whose objective is to search for fair rule lists approximating an unfair black-box model. We empirically evaluate our rationalization technique on black-box models trained on real-world datasets and show that one can obtain rule lists with high fidelity to the black-box model while being considerably less unfair at the same time.
  </details>
* [The (Un)reliability of Saliency Methods](https://www.researchgate.net/publication/335707891_The_Unreliability_of_Saliency_Methods#:~:text=Public)
  <details>
  <summary>P. J. Kindermans et al. <em>Explainable AI: Interpreting, Explaining and Visualizing Deep Learning</em> 2019 </summary>
  Saliency methods aim to explain the predictions of deep neural networks. These methods lack reliability when the explanation is sensitive to factors that do not contribute to the model prediction. We use a simple and common pre-processing step which can be compensated for easily—adding a constant shift to the input data—to show that a transformation with no effect on how the model makes the decision can cause numerous methods to attribute incorrectly. In order to guarantee reliability, we believe that the explanation should not change when we can guarantee that two networks process the images in identical manners. We show, through several examples, that saliency methods that do not satisfy this requirement result in misleading attribution. The approach can be seen as a type of unit test; we construct a narrow ground truth to measure one stated desirable property. As such, we hope the community will embrace the development of additional tests.
  </details>
* [Fooling Neural Network Interpretations via Adversarial Model Manipulation](http://papers.nips.cc/paper/8558-fooling-neural-network-interpretations-via-adversarial-model-manipulation#:~:text=pdf)
  <details>
  <summary>J. Heo et al. <em>Advances in Neural Information Processing Systems</em> 2019 </summary>
  We ask whether the neural network interpretation methods can be fooled via adversarial model manipulation, which is defined as a model fine-tuning step that aims to radically alter the explanations without hurting the accuracy of the original models, e.g., VGG19, ResNet50, and DenseNet121. By incorporating the interpretation results directly in the penalty term of the objective function for fine-tuning, we show that the state-of-the-art saliency map based interpreters, e.g., LRP, Grad-CAM, and SimpleGrad, can be easily fooled with our model manipulation. We propose two types of fooling, Passive and Active, and demonstrate such foolings generalize well to the entire validation set as well as transfer to other interpretation methods. Our results are validated by both visually showing the fooled explanations and reporting quantitative metrics that measure the deviations from the original explanations. We claim that the stability of neural network interpretation method with respect to our adversarial model manipulation is an important criterion to check for developing robust and reliable neural network interpretation method.
  </details>
* [Explanations can be manipulated and geometry is to blame](https://papers.nips.cc/paper/9511-explanations-can-be-manipulated-and-geometry-is-to-blame#:~:text=pdf)
  <details>
  <summary>A. K. Dombrowski et al. <em>Advances in Neural Information Processing System</em> 2019 </summary>
  Explanation methods aim to make neural networks more trustworthy and interpretable. In this paper, we demonstrate a property of explanation methods which is disconcerting for both of these purposes. Namely, we show that explanations can be manipulated arbitrarily by applying visually hardly perceptible perturbations to the input that keep the network's output approximately constant. We establish theoretically that this phenomenon can be related to certain geometrical properties of neural networks. This allows us to derive an upper bound on the susceptibility of explanations to manipulations. Based on this result, we propose effective mechanisms to enhance the robustness of explanations.
  </details>
  <p align="center"><img height='350' src="fig/attack.png"></p>
* [You Shouldn't Trust Me: Learning Models Which Conceal Unfairness From Multiple Explanation Methods](http://ecai2020.eu/papers/72_paper.pdf)
  <details>
  <summary>B. Dimanov et al. <em>European Conference on Artificial Intelligence</em> 2020 </summary>
  Transparency of algorithmic systems has been discussed as a way for end-users and regulators to develop appropriate trust in machine learning models. One popular approach, LIME [26], even suggests that model explanations can answer the question “Why should I trust you?” Here we show a straightforward method for modifying a pre-trained model to manipulate the output of many popular feature importance explanation methods with little change in accuracy, thus demonstrating the danger of trusting such explanation methods. We show how this explanation attack can mask a model’s discriminatory use of a sensitive feature, raising strong concerns about using such explanation methods to check model fairness.
  </details>
* [Fooling LIME and SHAP: Adversarial Attacks on Post hoc Explanation Methods](https://dl.acm.org/doi/10.1145/3375627.3375830#:~:text=pdf)
  <details>
  <summary>D. Slack et al. <em>AAAI/ACM Conference on AI, Ethics, and Society</em> 2020 </summary>
  As machine learning black boxes are increasingly being deployed in domains such as healthcare and criminal justice, there is growing emphasis on building tools and techniques for explaining these black boxes in an interpretable manner. Such explanations are being leveraged by domain experts to diagnose systematic errors and underlying biases of black boxes. In this paper, we demonstrate that post hoc explanations techniques that rely on input perturbations, such as LIME and SHAP, are not reliable. Specifically, we propose a novel scaffolding technique that effectively hides the biases of any given classifier by allowing an adversarial entity to craft an arbitrary desired explanation. Our approach can be used to scaffold any biased classifier in such a way that its predictions on the input data distribution still remain biased, but the post hoc explanations of the scaffolded classifier look innocuous. Using extensive evaluation with multiple real world datasets (including COMPAS), we demonstrate how extremely biased (racist) classifiers crafted by our framework can easily fool popular explanation techniques such as LIME and SHAP into generating innocuous explanations which do not reflect the underlying biases.
  </details>
* [“How do I fool you?": Manipulating User Trust via Misleading Black Box Explanations](https://dl.acm.org/doi/10.1145/3375627.3375833#:~:text=pdf)
  <details>
  <summary>H. Lakkaraju & O. Bastani <em>AAAI/ACM Conference on AI, Ethics, and Society</em> 2020 </summary>
  As machine learning black boxes are increasingly being deployed in critical domains such as healthcare and criminal justice, there has been a growing emphasis on developing techniques for explaining these black boxes in a human interpretable manner. There has been recent concern that a high-fidelity explanation of a black box ML model may not accurately reflect the biases in the black box. As a consequence, explanations have the potential to mislead human users into trusting a problematic black box. In this work, we rigorously explore the notion of misleading explanations and how they influence user trust in black box models. Specifically, we propose a novel theoretical framework for understanding and generating misleading explanations, and carry out a user study with domain experts to demonstrate how these explanations can be used to mislead users. Our work is the first to empirically establish how user trust in black box models can be manipulated via misleading explanations.
  </details>
* [Faking Fairness via Stealthily Biased Sampling](https://www.aaai.org/ojs/index.php/AAAI/article/view/5377#:~:text=pdf)
  <details>
  <summary>K. Fukuchi et al. <em>AAAI Conference on Artificial Intelligence</em> 2020 </summary>
  Auditing fairness of decision-makers is now in high demand. To respond to this social demand, several fairness auditing tools have been developed. The focus of this study is to raise an awareness of the risk of malicious decision-makers who fake fairness by abusing the auditing tools and thereby deceiving the social communities. The question is whether such a fraud of the decision-maker is detectable so that the society can avoid the risk of fake fairness. In this study, we answer this question negatively. We specifically put our focus on a situation where the decision-maker publishes a benchmark dataset as the evidence of his/her fairness and attempts to deceive a person who uses an auditing tool that computes a fairness metric. To assess the (un)detectability of the fraud, we explicitly construct an algorithm, the stealthily biased sampling, that can deliberately construct an evil benchmark dataset via subsampling. We show that the fraud made by the stealthily based sampling is indeed difficult to detect both theoretically and empirically.
  </details>
* [Sanity Checks for Saliency Metrics](https://www.aaai.org/ojs/index.php/AAAI/article/view/6064#:~:text=pdf)
  <details>
  <summary>R. Tomsett et al. <em>AAAI Conference on Artificial Intelligence</em> 2020 </summary>
  Saliency maps are a popular approach to creating post-hoc explanations of image classifier outputs. These methods produce estimates of the relevance of each pixel to the classification output score, which can be displayed as a saliency map that highlights important pixels. Despite a proliferation of such methods, little effort has been made to quantify how good these saliency maps are at capturing the true relevance of the pixels to the classifier output (i.e. their “fidelity”). We therefore investigate existing metrics for evaluating the fidelity of saliency methods (i.e. saliency metrics). We find that there is little consistency in the literature in how such metrics are calculated, and show that such inconsistencies can have a significant effect on the measured fidelity. Further, we apply measures of reliability developed in the psychometric testing literature to assess the consistency of saliency metrics when applied to individual saliency maps. Our results show that saliency metrics can be statistically unreliable and inconsistent, indicating that comparative rankings between saliency methods generated using such metrics can be untrustworthy.
  </details>
* [Fairwashing Explanations with Off-Manifold Detergent](https://proceedings.icml.cc/static/paper_files/icml/2020/3760-Paper.pdf)
  <details>
  <summary>C. J. Anderset al. <em>International Conference on Machine Learning</em> 2020 </summary>
  Explanation methods promise to make black-box classifiers more transparent. As a result, it is hoped that they can act as proof for a sensible, fair and trustworthy decision-making process of the algorithm and thereby increase its acceptance by the end-users. In this paper, we show both theoretically and experimentally that these hopes are presently unfounded. Specifically, we show that, for any classifier g, one can always construct another classifier g' which has the same behavior on the data (same train, validation, and test error) but has arbitrarily manipulated explanation maps. We derive this statement theoretically using differential geometry and demonstrate it experimentally for various explanation methods, architectures, and datasets. Motivated by our theoretical insights, we then propose a modification of existing explanation methods which makes them significantly more robust.
  </details>
* [Interpretable Deep Learning under Fire](https://www.usenix.org/conference/usenixsecurity20/presentation/zhang-xinyang#:~:text=pdf)
  <details>
  <summary>X. Zhang et al.<em>USENIX Security Symposium</em> 2020 </summary>
  Providing explanations for deep neural network (DNN) models is crucial for their use in security-sensitive domains. A plethora of interpretation models have been proposed to help users understand the inner workings of DNNs: how does a DNN arrive at a specific decision for a given input? The improved interpretability is believed to offer a sense of security by involving human in the decision-making process. Yet, due to its data-driven nature, the interpretability itself is potentially susceptible to malicious manipulations, about which little is known thus far. Here we bridge this gap by conducting the first systematic study on the security of interpretable deep learning systems (IDLSes). We show that existing IDLSes are highly vulnerable to adversarial manipulations. Specifically, we present ADV2, a new class of attacks that generate adversarial inputs not only misleading target DNNs but also deceiving their coupled interpretation models. Through empirical evaluation against four major types of IDLSes on benchmark datasets and in security-critical applications (e.g., skin cancer diagnosis), we demonstrate that with ADV2 the adversary is able to arbitrarily designate an input's prediction and interpretation. Further, with both analytical and empirical evidence, we identify the prediction-interpretation gap as one root cause of this vulnerability -- a DNN and its interpretation model are often misaligned, resulting in the possibility of exploiting both models simultaneously. Finally, we explore potential countermeasures against ADV2, including leveraging its low transferability and incorporating it in an adversarial training framework. Our findings shed light on designing and operating IDLSes in a more secure and informative fashion, leading to several promising research directions.
  </details>
* [The Bouncer Problem: Challenges to Remote Explainability](https://arxiv.org/abs/1910.01432#:~:text=pdf)
  <details>
  <summary>E. L. Merrer & G. Tredan <em>arXiv preprint v2</em> 2020 </summary>
  The concept of explainability is envisioned to satisfy society's demands for transparency on machine learning decisions. The concept is simple: like humans, algorithms should explain the rationale behind their decisions so that their fairness can be assessed. While this approach is promising in a local context (e.g. to explain a model during debugging at training time), we argue that this reasoning cannot simply be transposed in a remote context, where a trained model by a service provider is only accessible through its API. This is problematic as it constitutes precisely the target use-case requiring transparency from a societal perspective. Through an analogy with a club bouncer (which may provide untruthful explanations upon customer reject), we show that providing explanations cannot prevent a remote service from lying about the true reasons leading to its decisions. More precisely, we prove the impossibility of remote explainability for single explanations, by constructing an attack on explanations that hides discriminatory features to the querying user. We provide an example implementation of this attack. We then show that the probability that an observer spots the attack, using several explanations for attempting to find incoherences, is low in practical settings. This undermines the very concept of remote explainability in general.
  </details>

### Defense

* [Adversarial Explanations for Understanding Image Classification Decisions and Improved NN Robustness](https://arxiv.org/abs/1906.02896#:~:text=pdf)
  <details>
  <summary>W. Woods et al. <em>Nature Machine Intelligence</em> 2019 </summary>
  For sensitive problems, such as medical imaging or fraud detection, Neural Network (NN) adoption has been slow due to concerns about their reliability, leading to a number of algorithms for explaining their decisions. NNs have also been found vulnerable to a class of imperceptible attacks, called adversarial examples, which arbitrarily alter the output of the network. Here we demonstrate both that these attacks can invalidate prior attempts to explain the decisions of NNs, and that with very robust networks, the attacks themselves may be leveraged as explanations with greater fidelity to the model. We show that the introduction of a novel regularization technique inspired by the Lipschitz constraint, alongside other proposed improvements, greatly improves an NN's resistance to adversarial examples. On the ImageNet classification task, we demonstrate a network with an Accuracy-Robustness Area (ARA) of 0.0053, an ARA 2.4x greater than the previous state of the art. Improving the mechanisms by which NN decisions are understood is an important direction for both establishing trust in sensitive domains and learning more about the stimuli to which NNs respond.
  </details>
* [On the (In)fidelity and Sensitivity of Explanations](http://papers.nips.cc/paper/9278-on-the-infidelity-and-sensitivity-of-explanations#:~:text=pdf)
  <details>
  <summary>C. K. Yeh et al. <em>Advances in Neural Information Processing Systems</em> 2019 </summary>
  We consider objective evaluation measures of saliency explanations for complex black-box machine learning models. We propose simple robust variants of two notions that have been considered in recent literature: (in)fidelity, and sensitivity. We analyze optimal explanations with respect to both these measures, and while the optimal explanation for sensitivity is a vacuous constant explanation, the optimal explanation for infidelity is a novel combination of two popular explanation methods. By varying the perturbation distribution that defines infidelity, we obtain novel explanations by optimizing infidelity, which we show to out-perform existing explanations in both quantitative and qualitative measurements. Another salient question given these measures is how to modify any given explanation to have better values with respect to these measures. We propose a simple modification based on lowering sensitivity, and moreover show that when done appropriately, we could simultaneously improve both sensitivity as well as fidelity.
  </details>
* [A simple defense against adversarial attacks on heatmap explanations](https://arxiv.org/abs/2007.06381#:~:text=pdf)
  <details>
  <summary>L. Rieger & L. K. Hansen <em>ICML Workshop on Human Interpretability in Machine Learning</em> 2020 </summary>
  With machine learning models being used for more sensitive applications, we rely on interpretability methods to prove that no discriminating attributes were used for classification. A potential concern is the so-called "fair-washing" - manipulating a model such that the features used in reality are hidden and more innocuous features are shown to be important instead. In our work we present an effective defence against such adversarial attacks on neural networks. By a simple aggregation of multiple explanation methods, the network becomes robust against manipulation. This holds even when the attacker has exact knowledge of the model weights and the explanation methods used.
  </details>
  <p align="center"><img height='350' src="fig/defense.png"></p>
* [Proper Network Interpretability Helps Adversarial Robustness in Classification](https://proceedings.icml.cc/static/paper_files/icml/2020/1661-Paper.pdf)
  <details>
  <summary>A. Boopathy et al. <em>International Conference on Machine Learning</em> 2020 </summary>
  Recent works have empirically shown that there exist adversarial examples that can be hidden from neural network interpretability (namely, making network interpretation maps visually similar), or interpretability is itself susceptible to adversarial attacks. In this paper, we theoretically show that with a proper measurement of interpretation, it is actually difficult to prevent prediction-evasion adversarial attacks from causing interpretation discrepancy, as confirmed by experiments on MNIST, CIFAR-10 and Restricted ImageNet. Spurred by that, we develop an interpretability-aware defensive scheme built only on promoting robust interpretation (without the need for resorting to adversarial loss minimization). We show that our defense achieves both robust classification and robust interpretation, outperforming state-of-theart adversarial training methods against attacks of large perturbation in particular.
  </details>
* [Aggregating explanation methods for stable and robust explainability](https://arxiv.org/abs/1903.00519#:~:text=pdf)
  <details>
  <summary>L. Rieger & L. K. Hansen <em>arXiv preprint v5</em> 2020 </summary>
  Despite a growing literature on explaining neural networks, no consensus has been reached on how to explain a neural network decision or how to evaluate an explanation. Our contributions in this paper are twofold. First, we investigate schemes to combine explanation methods and reduce model uncertainty to obtain a single aggregated explanation. We provide evidence that the aggregation is better at identifying important features, than on individual methods. Adversarial attacks on explanations is a recent active research topic. As our second contribution, we present evidence that aggregate explanations are much more robust to attacks than individual explanation methods.
  </details>

### Other

* [Evaluating Explanation Methods for Deep Learning in Security](https://arxiv.org/abs/1906.02108#:~:text=pdf)
  <details>
  <summary>A. Warnecke et al. <em>IEEE European Symposium on Security and Privacy</em> 2020</summary>
  Deep learning is increasingly used as a building block of security systems. Unfortunately, neural networks are hard to interpret and typically opaque to the practitioner. The machine learning community has started to address this problem by developing methods for explaining the predictions of neural networks. While several of these approaches have been successfully applied in the area of computer vision, their application in security has received little attention so far. It is an open question which explanation methods are appropriate for computer security and what requirements they need to satisfy. In this paper, we introduce criteria for comparing and evaluating explanation methods in the context of computer security. These cover general properties, such as the accuracy of explanations, as well as security-focused aspects, such as the completeness, efficiency, and robustness. Based on our criteria, we investigate six popular explanation methods and assess their utility in security systems for malware detection and vulnerability discovery. We observe significant differences between the methods and build on these to derive general recommendations for selecting and applying explanation methods in computer security.
  </details>
* [Evaluating and Aggregating Feature-based Model Explanations](https://arxiv.org/abs/2005.00631#:~:text=pdf)
  <details>
  <summary>U. Bhatt et al. <em>arXiv preprint v1</em> 2020</summary>
  A feature-based model explanation denotes how much each input feature contributes to a model's output for a given data point. As the number of proposed explanation functions grows, we lack quantitative evaluation criteria to help practitioners know when to use which explanation function. This paper proposes quantitative evaluation criteria for feature-based explanations: low sensitivity, high faithfulness, and low complexity. We devise a framework for aggregating explanation functions. We develop a procedure for learning an aggregate explanation function with lower complexity and then derive a new aggregate Shapley value explanation function that minimizes sensitivity.
  </details>

## Software

...
