 python3 create_lmdb_dataset.py --inputPath data/train --gtFile data/train/gt.txt --outputPath result/train
 python3 create_lmdb_dataset.py --inputPath data/valid --gtFile data/valid/gt.txt --outputPath result/valid                                                     

space must be included in character and I can tune batch size with --batch_max_length

python3 train.py --train_data result/train --valid_data result/valid --Transformation None --FeatureExtraction VGG --SequenceModeling BiLSTM --Prediction CTC --workers=0 --batch_max_length 60
