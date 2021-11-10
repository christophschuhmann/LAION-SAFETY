# LAION-SAFETY
A open toolbox for NSFW &amp; toxicity detection

# Overview
We present an ensemble of a NSFW image classifier ( based on EfficientNet V2, https://github.com/google/automl/tree/master/efficientnetv2 ) together with Detoxify ( https://github.com/unitaryai/detoxify ), an existing language model for toxicity detection.

The image classifier had been trained on XXX images from the 5 classes "Drawing" ( ), "Hentai" ( ), "Neutral" ( ), "Porn" ( ) & "Sexy" ( ).

To evaluate the performance of the image classifier together with & without additional information from Detoxify, we created a manually  inspected test set that consists of XXXX samples, that contains images & their captions.

![image](https://cdn.discordapp.com/attachments/893170386030694460/908071613520560160/unknown.png)

To use our 5 class image classifier as a binary SFW - NSFW classifier, we consider images from the classes "Drawing" & "Neutral" as SFW and "Hentai", "Porn" & "Sexy" as NSFW.

--> Our image classifier predicts XX % of the true NSFW correctly as NSFW (false negatives) and discards XX % of the SFW images incorrectly as NSFW (false positives).

We compare our model with XXXXX Gantman XXXXX , to our knowledge the best openly available NSFW classifier at the time of writing:

![image](https://cdn.discordapp.com/attachments/893170386030694460/905489671654613102/unknown.png)

False negatives:
False positives:
 
--> Our image classifier predicts XX % less false negatives & XX % less false positives.


To leverage the information from the image captions, we add the sum of Detoxify's "toxicity" & "sexual_explicity" scores to the softmax scores of the image classifier before determining the category with the highest score.

This ensemble archives the following performance:

![image](https://cdn.discordapp.com/attachments/893170386030694460/908072103465599026/unknown.png)

False negatives:
False positives:

--> This ensemble predicts XX % less false negatives & XX % less false positives.


# Inference



# Training



# Disclaimer
Even though this is obvious, we explicitly state here that the predictions made by our image classifier & its ensemble with Detoxify are not 100% correct & that everyone who applies them has to take the full responsibilty for this application. 
