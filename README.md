# widerface-matlab-evaluate
Matlab code for evaluating the widerface dataset

## Requirements

A feasible solution is matlab R2016a under window11

## wider_eval.m

During use, you should pay attention to the wider_eval.m file. 

For the val set, 

1. you should modify the ```pred_dir = './pred';``` part in wider_eval.m. 

For the test set, 

1. The results of the official server test need to be placed in the corresponding location in the ```./eval_tools/plot/baselines/Test directory```; 

2. The code related to the val part should be commented out, for example: 

  ```% legend_name = 'Faceness';
  % for i = 1:size(setting_name_list,1)
  %     fprintf('Current evaluation setting %s\n',setting_name_list{i});
  %     setting_name = setting_name_list{i};
  %     gt_dir = sprintf('./ground_truth/wider_%s.mat',setting_name);
  %     evaluation(norm_pred_list,gt_dir,setting_name,setting_class,legend_name);
  % end
  ```

3. You also need to modify
  ```setting_name_list = {'easy_val';'medium_val';'hard_val'};```; to ```setting_name_list = {'easy';'medium';'hard'}; ```

4. Change ```dateset_class = 'Val';``` to ```dateset_class = 'Test'```;

## Citations

```
@inproceedings{yang2016wider,
	Author = {Yang, Shuo and Luo, Ping and Loy, Chen Change and Tang, Xiaoou},
	Booktitle = {IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
	Title = {WIDER FACE: A Face Detection Benchmark},
	Year = {2016}}
```

