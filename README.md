# Picrust2
16s数据的功能预测
https://github.com/picrust/picrust2/wiki/Metagenome-prediction  
安装miniconda  
mkdir -p ~/miniconda3 # 这个命令创建一个名为 miniconda3 的目录（文件夹）在你的用户主目录 (~) 下。这将用于存储 Miniconda 安装
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh

metagenome_pipeline.py -i ~/data/projects/innoihealth/Yaoming_B_16S/input/nfcore_16s/picrust2/feature-table.biom \
                       -m ~/data/projects/innoihealth/Yaoming_B_16S/input/nfcore_16s/picrust2/marker_predicted_and_nsti.tsv.gz \
                       -f ~/data/projects/innoihealth/Yaoming_B_16S/input/nfcore_16s/picrust2/KO_predicted.tsv.gz \
                       -o ~/data/projects/innoihealth/Yaoming_B_16S/input/nfcore_16s/picrust2/KO_metagenome_out2 \
                       --strat_out
