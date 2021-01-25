# FDL 2021 Competition

This repository contains the data, code and model used for the FDL kaggle competition as well as the report.
It is organized as follows:
```
FDL_competition/
|_ mlruns/                                     <- folder containing the various models tested and their characteristics and performance (hyperparameters, best validation loss, best model over all epochs and loss chart). For space saving reasons, only the final model was kept.
|_ output/                                     <- the model's predicted masks as .png images
|  |_ postprocessed/                           <- the model's predicted masks after postprocessing (morphological transformations) as .png images. For space saving reasons, this folder was emptied.
|_ test_images/		  
|_ train_images/
|  |_ augmented/                               <- the images resulting from the data augmentation process (rotated versions of some images). For space saving reasons, this folder was emptied.
|_ train_masks/
|  |_ augmented/                               <- the masks corresponding to the augmented images. For size reasons, this folder was emptied.
|_ unet/                                       <- code for the UNet model
|_ utils/                       
|  |_ dice_loss.py                             <- pytorch implementation of the dice loss
|  |_ evaluation.py                            <- functions used to evaluate the model
|  |_ postprocessing.py                        <- functions used to perform morphological transformations on the predicted masks
|  |_ preprocessing.py                         <- dataloader and functions used to perform data augmentation/channel-wise normalization on the images
|  |_ submit.py  
|_ FDL_competition-report_Corentin-MARY.pdf    <- the report                
|_ mlflow_tracking.ipynb                       <- notebook to observe and compare the results form the different runs using mlflow
|_ submission.ipynb                            <- notebook used to run the model on the test set and prepare the submission file
|_ training.ipynb                              <- notebook to train the model
```

To reproduce the results, import the folder on your Google Drive and run the submission notebook in Colab (skip the "Postprocessing" part as it is does not improve the model's performance). 
