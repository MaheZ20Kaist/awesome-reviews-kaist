---
description: Hendrycks / Deep Anomaly Detection using Outlier Exposure / ICLR 2019
---



##  1. Problem definition

Detection of Out-Of-Distribution data is of paramount importance. Despite numerous researches in the domain, it is not possible to make outlier detectors learn representations or gain knowledge of out-of-distribution data beforehand. Anomaly detection problems have previously been explored with the usage of Deep Learning classifiers which assigns anomaly scores to inputs. They do so by using knowledge from in-distribution data. However, in the real world outlier distributions are imperceptible by the detector and this necessitates a reciprocal method that could potentially handle it. 


## 2. Motivation


### Related work
 Hendrycks et al. proposed the usage of Maximum Softmax Probability of prediction to evaluate whether the example is out-of-distribution[1]. The MSP will have a lower softmax probability on samples that are out of distribution. It is also possible to use a supplementary branch on the pre-trained classifier and produce a OOD score[2]. By using adversarial perturbations on the input data [3], Goodfellow et al. successfully made the maximum softmax probability between in-distribution data and OOD more distinctive. In object detection tasks, models often classify OOD samples with high confidence therefore Lee et al. trains GAN concurrently with a classifier [4] and this results in the classifier having lower confidence for the GAN samples. 
 Salakhutdinov et al. pre trained deep learning classifier on web images to learn feature representations[5], Zeiler & Fergus et al. pre-trained on ImageNet and deems it useful for fine tuning applications[6]. Similarly, Radford et al. pretrained unsupervised networks on Amazon reviews to acquire customer sentiment representations which could further be fine-tuned on sentiment analysis tasks[7]. 


### Idea

The authors make use of Outlier Exposure which uses supplementary datasets because in reality, OOD data that can potentially be encountered remains unknown. Therefore the procedure makes use of an auxiliary dataset or Outlier Exposure dataset that is  different from the OOD test data to be used and an in-distribution dataset. Therefore, the objective is to minimize the following loss function:
!()[loss.png]

## 3. Method

{% hint style="info" %}
If you are writing **Author's note**, please share your know-how \(e.g., implementation details\)
{% endhint %}

The proposed method of the paper will be depicted in this section.

Please note that you can attach image files \(see Figure 1\).  
When you upload image files, please read [How to contribute?](../../how-to-contribute.md#image-file-upload) section.

![Figure 1: You can freely upload images in the manuscript.](../../.gitbook/assets/how-to-contribute/cat-example.jpg)

We strongly recommend you to provide us a working example that describes how the proposed method works.  
Watch the professor's [lecture videos](https://www.youtube.com/playlist?list=PLODUp92zx-j8z76RaVka54d3cjTx00q2N) and see how the professor explains.

## 4. Experiment & Result

{% hint style="info" %}
If you are writing **Author's note**, please share your know-how \(e.g., implementation details\)
{% endhint %}

This section should cover experimental setup and results.  
Please focus on how the authors of paper demonstrated the superiority / effectiveness of the proposed method.

Note that you can attach tables and images, but you don't need to deliver all materials included in the original paper.

### Experimental setup

This section should contain:

* Dataset
* Baselines
* Training setup
* Evaluation metric
* ...

### Result

Please summarize and interpret the experimental result in this subsection.

## 5. Conclusion

In conclusion, please sum up this article.  
You can summarize the contribution of the paper, list-up strength and limitation, or freely tell your opinion about the paper.

### Take home message \(오늘의 교훈\)

Please provide one-line \(or 2~3 lines\) message, which we can learn from this paper.

> All men are mortal.
>
> Socrates is a man.
>
> Therefore, Socrates is mortal.

## Author / Reviewer information

{% hint style="warning" %}
You don't need to provide the reviewer information at the draft submission stage.
{% endhint %}

### Author

**Korean Name \(English name\)** 

* Affiliation \(KAIST AI / NAVER\)
* \(optional\) 1~2 line self-introduction
* Contact information \(Personal webpage, GitHub, LinkedIn, ...\)
* **...**

### Reviewer

1. Korean name \(English name\): Affiliation / Contact information
2. Korean name \(English name\): Affiliation / Contact information
3. ...

## Reference & Additional materials

1. Citation of this paper
2. Official \(unofficial\) GitHub repository
3. Citation of related work
4. Other useful materials
5. ...

