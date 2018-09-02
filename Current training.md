# Current training so far

__Rounds 1 and 2 were recording to the same log file original, this has now been changed from round 3 (which to confuse things is log 2)__

1. First round of training was initially to understand if the model was working and to gain some level of understanding over the initial implementation.

Round 1 was assigned the default options of 50 epochs (stage 1) for frozen layers except for the last 3 (249 frozen out of 252 layers) and then 50 epochs all unfrozen (stage 2).

Stage 1 Runs for 50 epochs freezing the first 249 layers of total 252 layers.

Trains on 94 samples, and validation is 10 samples, with batch size 32.

Stage 1 loss @ 86.2202, val_loss @ 75.4246

Stage 2 loss @ 21.1380 val_loss @ 21.8380 (at 70/100 epochs)

2. Increased training to 100 epochs on stage 1 and training was also increased on (stage 2).

Stage 1 loss @ ~21.00
Stage 2 early stopping @ 153 epochs loss @ 15.8775, 17.5058

3. Dataset is currently imbalanced as
    * speed sign: 67
    * sharp deviation of route sign: 25
    * no entry sign: 15
    
    updated and added more signs to the data set as well as new classes, whilst dataset is still unbalanced attempting to understand if that is an actual immediate factor or if that's a different problem.

    * speed sign: 254
    * sharp deviation of route sign: 186
    * give way sign: 12
    * no entry sign: 43
    * keep left sign: 55

    550 images will now be trained on the original 50 epochs stage 1 and 50 epochs stage 2.

    Logs are stored in logs/2