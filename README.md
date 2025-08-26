# 👋 你好，我是 liuqingshan

<img align="right" alt="coding" src="/assets/coding.gif" width="320px" />

生物信息工程师，专注于遗传病诊断、肿瘤分子检测与病原微生物分析；长期从事实验室落地与生产级流水线建设，并在生信算法工程化与高性能优化（Rust 等）方面有深入实践。

- 🔬 方向：遗传诊断 | 肿瘤检测 | 病原微生物 | 长读长分析
- ⚙️ 强项：算法优化与工程化 | 高性能实现（Rust）| 流水线标准化与可复现
- 🌱 近期：长读长在罕见病中的临床转化与结构变异检测优化
- 🤝 合作：面向生产环境的流程搭建、性能加速与算法攻关

---

## 领域能力

- 遗传病诊断
  - WES/WGS/长读长（ONT/PacBio HiFi）变异检测：SNV/Indel/CNV/SV/Repeat 扩增与相位
  - 结构变异与重复扩增：cuteSV/Sniffles/SVIM、ExpansionHunter、WhatsHap
  - 变异注释与临床级解释：VEP/ANNOVAR，HGVS、ACMG/AMP 标准，ClinVar/OMIM/gnomAD/ClinGen
- 肿瘤分子检测
  - ctDNA/MRD/靶向 Panel/外显子组/WGS；UMI/双链纠错；亚克隆与超低频突变
  - CNV/TMB/MSI/HRD，融合检测（STAR-Fusion/Arriba），拷贝数（CNVkit/FACETS/ichorCNA）
- 病原微生物检测
  - mNGS/宏基因组/扩增子；鉴定、分型、耐药与毒力基因、混合感染与低丰度检出
  - 参考数据库治理、污染去除、宿主去除与批量化分析
- 工程化与合规
  - 流水线标准化、可追溯与版本化（Nextflow/Snakemake + Docker/Singularity）
  - 数据与格式：FASTQ/BAM/CRAM/VCF、HGVS、GA4GH 生态；IGV 证据链与报告自动化
  - 质量控制与稳健性：覆盖度/深度/bias 监控、批次效应、模拟与回归测试

## 技术栈

- 语言与并行
  - Rust（Rayon/tokio、SIMD/AVX2/AVX-512、零拷贝 I/O、内存池化）
  - Python（科学计算/原型验证）、Bash、R；必要时 C/C++
- 平台与基础设施
  - HPC/集群（Slurm）、容器（Docker/Singularity）、CI/CD（GitHub Actions）
  - 数据版本化与可复现（DVC/conda/mamba）、性能剖析（perf/flamegraph/pprof）
- 经典工具与框架
  - 比对：BWA-MEM2、minimap2、STAR、Bowtie2
  - 变异检测：GATK、DeepVariant、Strelka2、FreeBayes、Manta、Mutect2
  - 结构变异/拷贝数/融合：cuteSV、Sniffles、SVIM、CNVkit、FACETS、ichorCNA、STAR-Fusion、Arriba
  - 长读长与甲基化：Flye/hifiasm、Medaka/Clair3、megalodon/nanopolish
  - mNGS/宏基因组：Kraken2/Bracken、Centrifuge、MetaPhlAn、HUMAnN
  - 注释与 QC：VEP/ANNOVAR、bcftools/samtools、FastQC/MultiQC、mosdepth

## 代表项目

- 罕见病长读长全流程
  - ONT/PacBio 端到端流程：比对→SV/重复扩增→相位→注释→报告
  - 在真实临床样本中提升复杂结构变异与重复扩增的检出稳定性
- 肿瘤 UMI/双链 MRD 流程
  - 超低频变异建模与误差校正，融合/拷贝数/TMB/MSI 一体化报告
  - 引入“证据链”导出（BAM 片段、IGV 快照）支撑临床复核
- 高性能微生物鉴定与去宿主
  - Rust 实现的高速 I/O、并行 k-mer/最小化子索引、Bloom 过滤
  - 在大体量样本与海量数据库场景显著降本增效
- WES/WGS 标准化流水线
  - Nextflow + 容器化 + CI/CD + 数据版本化，支持生产级稳健运行
  - 内建 QC/门限校准/回归测试，便于审计与合规

## 性能优化要点

- 算法：最小化子索引、向量化 DP/比对内核、近似去噪与自适应阈值
- 并行：分片调度、工作窃取、CPU 亲和性；I/O 与计算重叠
- I/O：mmap/零拷贝、bgzip/多线程压缩、块级缓存与布局友好数据结构
- 剖析与稳定性：perf/flamegraph、基准测试、长尾样本防抖与限流

## 开源与分享

- 工具/流水线：变异检测与注释工具、mNGS/长读长流程、VCF/BAM 实用脚本
- 文章/分享：标准化流程落地、长读长在临床中的实践、Rust 在生信的性能优势

## 如何合作

- 流水线从 0 到 1：需求梳理→设计评审→原型→生产化→合规与交付
- 现有流程加速与稳健性改造：性能剖析→瓶颈定位→算法/工程优化→回归测试
- 专题攻关：结构变异/重复扩增、低频变异、mNGS 低丰度检出

## 联系方式

- 📫 Email：请在 Issue 或 Profile 联系方式中与我取得联系
- 💬 欢迎就算法、工程化与性能优化相关话题交流
