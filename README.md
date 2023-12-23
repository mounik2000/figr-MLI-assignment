# ML Intern Assignment for Figr

Assignment Link: https://prokit.notion.site/ML-Intern-Assignment-1ba4146a92a94cd88d8849158eb16912

Implementation details: Run the notebook in the presence of GPUs

## Key Details
1. Considering the GPU and RAM limitations, I used the Falcon-7B 4-bit model. (Local doesn't have GPUs; used free collab GPU)
2. I wrote the logic for training in PyTorch instead of using inbuilt HF trainers.
3. Used Dynamic Learning Rate Scheduler with Adam optimizer
4. Here is the code to compute the BLEU score. We used this to compare two html codes (two strings).
<img width="500" alt="image" src="https://github.com/mounik2000/figr-MLI-assignment/assets/57180667/bc1c2e95-97a3-4bf8-bb29-f11ee78824cc">

## Challenges Faced
1. Saving the model for the API: The 4-bit model config cannot be saved from Collab
2. Running the code to compute the metric: There were some compilation issues for a long time, and the test results could have been better. (see the last two cells of the notebook). Hence included the code separately
3. Training: The time taken was too long for multiple epochs, and some tokenizer issues while increasing the batch size, manually setting the batch size to one. (This should be fixed if more time was put into this assignment)
### Tasks completed
Script for preprocessing, fine-tuning, training, and inference of the model
### Tasks incomplete
1. Couldn't develop the API as the 4-bit model cannot be saved. Increasing the size requires higher GPU access.
2. Couldn't run for multiple epochs as the time taken for each epoch is very long.
3. Evaluating the metric values.
4. Code can be optimized (some redundancy)
