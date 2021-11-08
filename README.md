# Epilepsy-Seizure-Classification

Epilepsy
Epilepsy may occur as a result of a genetic disorder or an acquired brain injury, such as a trauma or stroke. During a seizure, a person experiences abnormal behaviour, symptoms and sensations, sometimes including loss of consciousness. There are few symptoms between seizures. Epilepsy is usually treated by medication and in some cases by surgery, devices or dietary changes.

Seizure
A seizure is a sudden surge of electrical activity in the brain. A seizure usually affects how a person appears or acts for a short time. Many different things can occur during a seizure. Whatever the brain and body can do normally can also occur during a seizure.

Detection
Epilepsy is the second most common brain disorder after migraine. Automatic detection of epileptic seizures can considerably improve the patients’ quality of life. CurrentElectroencephalogram (EEG)-based seizure detection systems encounter many challenges in real-life situations. The EEGs are non-stationary signals and seizure patterns vary across patients and recording sessions. Moreover, EEG data are prone to numerous noise types that negatively affect the detection accuracy of epileptic seizures. To address these challenges, we introduce the use of a deep learning-based approach that automatically learns the discriminative EEG features of epileptic seizures. Specifically, to reveal the correlation between successive data samples, Long Short-Term Memory (LSTM) network is used to learn the high-level representations of the normal and the seizure EEG patterns. Secondly, these representations are fed into Softmax function for training and classification.

Dataset
data.csv UCI Machine Repository - Epileptic Seizure Recognition Data Set
The original dataset from the reference consists of 5 different folders, each with 100 files, with each file representing a single subject/person. Each file is a recording of brain activity for 23.6 seconds. The corresponding time-series is sampled into 4097 data points. Each data point is the value of the EEG recording at a different point in time. So we have total 500 individuals with each has 4097 data points for 23.5 seconds. We divided and shuffled every 4097 data points into 23 chunks, each chunk contains 178 data points for 1 second, and each data point is the value of the EEG recording at a different point in time. So now we have 23 x 500 = 11500 pieces of information(row), each information contains 178 data points for 1 second(column), the last column represents the label y {1,2,3,4,5}. The response variable is y in column 179, the Explanatory variables X1, X2, ..., X178 y contains the category of the 178-dimensional input vector. Specifically y in {1, 2, 3, 4, 5}: 5 - eyes open, means when they were recording the EEG signal of the brain the patient had their eyes open
4 - eyes closed, means when they were recording the EEG signal the patient had their eyes closed
3 - Yes they identify where the region of the tumor was in the brain and recording the EEG activity from the healthy brain area
2 - They recorded the EEG from the area where the tumor was located
1 - Recording of seizure activity
All subjects falling in classes 2, 3, 4, and 5 are subjects who did not have epileptic seizure. Only subjects in class 1 have epileptic seizure. Our motivation for creating this version of the data was to simplify access to the data via the creation of a .csv version of it. Although there are 5 classes most authors have done binary classification, namely class 1 (Epileptic seizure) against the rest.
