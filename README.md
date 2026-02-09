#整体结构

##机器人描述文件

采用的是Isaaclab进行训练，所以要是想训练新的机器人的话，首先找到/home/user/Isaaclab/unitree_rl_lab/source/unitree_rl_lab/unitree_rl_lab/assets/robots/unitree.py这个文件，这个文件存放了所有机器人的URDF

##任务文件

所有的任务按照locomotion和mimic被分为了两个部分，此处以locomotion为例
agents里面存放的是rsl_rl框架的配置文件
mdp里面存放的是训练时的奖励惩罚设置
robots里面就是具体的机器人对应的环境和参数设置，还有任务设置

#训练

在经过上述的文件更改后，即可进行新任务的训练，运行
python scripts/rsl_rl/train.py  --task Unitree-R1-26dof-Velocity
即可开始训练
#回放

运行下述命令即可回放观察效果
python scripts/rsl_rl/play.py --task Unitree-R1-26dof-Velocity --load_run <你的日期时间文件夹名>

#Sim2Sim
coming soon
