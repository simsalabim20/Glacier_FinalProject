Everything important is in CNN_classification




Jonas files and solutions

Jonas Thickness_NN_crude.ipynb. 
H-parameters: {activation: ‘relu’, hidden_layers: (75, 75) , back_propagation: 50}, no optimization/CV.
Early stopping patience = 10, didn’t trigger.
mae = 42.92 and R2 = 0.669.
Run time:

Termtype CNN + NN 100.00 % accuracy w/ & wo/ CNN
__________________________________________________________________________________________________
 Layer (type)                   Output Shape         Param #     Connected to                     
==================================================================================================
 input_27 (InputLayer)          [(None, 64, 64, 1)]  0           []                               
                                                                                                  
 conv2d_80 (Conv2D)             (None, 62, 62, 32)   320         ['input_27[0][0]']               
                                                                                                  
 max_pooling2d_80 (MaxPooling2D  (None, 31, 31, 32)  0           ['conv2d_80[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_81 (Conv2D)             (None, 29, 29, 64)   18496       ['max_pooling2d_80[0][0]']       
                                                                                                  
 max_pooling2d_81 (MaxPooling2D  (None, 14, 14, 64)  0           ['conv2d_81[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_82 (Conv2D)             (None, 12, 12, 128)  73856       ['max_pooling2d_81[0][0]']       
                                                                                                  
 max_pooling2d_82 (MaxPooling2D  (None, 6, 6, 128)   0           ['conv2d_82[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_83 (Conv2D)             (None, 4, 4, 256)    295168      ['max_pooling2d_82[0][0]']       
                                                                                                  
 max_pooling2d_83 (MaxPooling2D  (None, 2, 2, 256)   0           ['conv2d_83[0][0]']              
 )                                                                                                
                                                                                                  
 flatten_20 (Flatten)           (None, 1024)         0           ['max_pooling2d_83[0][0]']       
                                                                                                  
 dense_89 (Dense)               (None, 64)           65600       ['flatten_20[0][0]']             
                                                                                                  
 input_28 (InputLayer)          [(None, 53)]         0           []                               
                                                                                                  
 concatenate_13 (Concatenate)   (None, 117)          0           ['dense_89[0][0]',               
                                                                  'input_28[0][0]']               
                                                                                                  
 dense_90 (Dense)               (None, 117)          13806       ['concatenate_13[0][0]']         
                                                                                                  
 dense_91 (Dense)               (None, 180)          21240       ['dense_90[0][0]']               
                                                                                                  
 dense_93 (Dense)               (None, 32)           5792        ['dense_91[0][0]']               
                                                                                                  
 dense_94 (Dense)               (None, 4)            132         ['dense_93[0][0]']               
                                                                                                  
==================================================================================================

Form CNN + NN 100.00 % accuracy w/ & wo/ CNN
__________________________________________________________________________________________________
 Layer (type)                   Output Shape         Param #     Connected to                     
==================================================================================================
 input_23 (InputLayer)          [(None, 64, 64, 1)]  0           []                               
                                                                                                  
 conv2d_72 (Conv2D)             (None, 62, 62, 32)   320         ['input_23[0][0]']               
                                                                                                  
 max_pooling2d_72 (MaxPooling2D  (None, 31, 31, 32)  0           ['conv2d_72[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_73 (Conv2D)             (None, 29, 29, 64)   18496       ['max_pooling2d_72[0][0]']       
                                                                                                  
 max_pooling2d_73 (MaxPooling2D  (None, 14, 14, 64)  0           ['conv2d_73[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_74 (Conv2D)             (None, 12, 12, 128)  73856       ['max_pooling2d_73[0][0]']       
                                                                                                  
 max_pooling2d_74 (MaxPooling2D  (None, 6, 6, 128)   0           ['conv2d_74[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_75 (Conv2D)             (None, 4, 4, 256)    295168      ['max_pooling2d_74[0][0]']       
                                                                                                  
 max_pooling2d_75 (MaxPooling2D  (None, 2, 2, 256)   0           ['conv2d_75[0][0]']              
 )                                                                                                
                                                                                                  
 flatten_18 (Flatten)           (None, 1024)         0           ['max_pooling2d_75[0][0]']       
                                                                                                  
 dense_77 (Dense)               (None, 64)           65600       ['flatten_18[0][0]']             
                                                                                                  
 input_24 (InputLayer)          [(None, 53)]         0           []                               
                                                                                                  
 concatenate_11 (Concatenate)   (None, 117)          0           ['dense_77[0][0]',               
                                                                  'input_24[0][0]']               
                                                                                                  
 dense_78 (Dense)               (None, 117)          13806       ['concatenate_11[0][0]']         
                                                                                                  
 dense_79 (Dense)               (None, 180)          21240       ['dense_78[0][0]']               
                                                                                                  
 dense_81 (Dense)               (None, 32)           5792        ['dense_79[0][0]']               
                                                                                                  
 dense_82 (Dense)               (None, 1)            33          ['dense_81[0][0]']               
                                                                                                  
==================================================================================================

### THIS RESULT IS WITH 0 THICKNESS PICTURES AND MEASUREMENTS. REMOVING THIS WILL IMPROVE IT
THICKNESS NN + CNN MAE on validation 33.9 m
Trained for 4.5 hours
__________________________________________________________________________________________________
 Layer (type)                   Output Shape         Param #     Connected to                     
==================================================================================================
 input_27 (InputLayer)          [(None, 64, 64, 1)]  0           []                               
                                                                                                  
 conv2d_80 (Conv2D)             (None, 62, 62, 32)   320         ['input_27[0][0]']               
                                                                                                  
 max_pooling2d_80 (MaxPooling2D  (None, 31, 31, 32)  0           ['conv2d_80[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_81 (Conv2D)             (None, 29, 29, 64)   18496       ['max_pooling2d_80[0][0]']       
                                                                                                  
 max_pooling2d_81 (MaxPooling2D  (None, 14, 14, 64)  0           ['conv2d_81[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_82 (Conv2D)             (None, 12, 12, 128)  73856       ['max_pooling2d_81[0][0]']       
                                                                                                  
 max_pooling2d_82 (MaxPooling2D  (None, 6, 6, 128)   0           ['conv2d_82[0][0]']              
 )                                                                                                
                                                                                                  
 conv2d_83 (Conv2D)             (None, 4, 4, 256)    295168      ['max_pooling2d_82[0][0]']       
                                                                                                  
 max_pooling2d_83 (MaxPooling2D  (None, 2, 2, 256)   0           ['conv2d_83[0][0]']              
 )                                                                                                
                                                                                                  
 flatten_20 (Flatten)           (None, 1024)         0           ['max_pooling2d_83[0][0]']       
                                                                                                  
 dense_89 (Dense)               (None, 64)           65600       ['flatten_20[0][0]']             
                                                                                                  
 input_28 (InputLayer)          [(None, 53)]         0           []                               
                                                                                                  
 concatenate_13 (Concatenate)   (None, 117)          0           ['dense_89[0][0]',               
                                                                  'input_28[0][0]']               
                                                                                                  
 dense_90 (Dense)               (None, 117)          13806       ['concatenate_13[0][0]']         
                                                                                                  
 dense_91 (Dense)               (None, 180)          21240       ['dense_90[0][0]']               
                                                                                                  
 dense_93 (Dense)               (None, 32)           5792        ['dense_91[0][0]']               
                                                                                                  
 dense_94 (Dense)               (None, 1)            33          ['dense_93[0][0]']               
                                                                                                  
==================================================================================================
