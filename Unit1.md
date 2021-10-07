# An Introduction to Computer Science <br> (Foundations of Computer Science) <br> 计算机科学导论

---

# QQ Group

<img src="figs/QQ-Group.jpg" alt="QQ-Group" width="300">

## Chinese students :  Please join this QQ group

## International students :  Not need to join this QQ group

---

# The Text book 

##  Title :  **An Introduction to Computer Science (English-Chinese Bilingual)**

## 计算机科学导论（英中双语版）

<img src="figs/TextBook.png" alt="TextBook" width="300">

<https://item.jd.com/12055742.html>

---

# The Text Book 

## $16$ chapters/units, divided into $6$ parts: 

- <mark>**Preface and Introduction** (Preface and Unit $1$) </mark>
- <mark>**Data representation and Operation** (Units $2 \sim 4$) </mark>
- Computer **Hardware** (Units $5 \sim 6$)
- Computer **Software** (Units $7 \sim 10$)
- **Data Organization** and Abstraction (units $11 \sim 12$)
- Advanced and Hot Topics (e.g., **Internet of Things**, **Cloud Computing**, and **Big Data** etc.) (Units $ 13 \sim 16$)

---

# The Reference  Book 

## 计算机科学导论

<img src="figs/TextBook_CR.jpg" alt="TextBook" width="300">

https://item.jd.com/59142846589.html

##  Title :  **Foundations of  Computer Science -- From Data Manipulation to Theory of Computation**

---

# Unit 1 Introduction <br> 第一章 绪论

---

# What Is Computer Science?

## **Computer science** is <mark>the study of computation and information. </mark>
<!--- a discipline that involves the theoretical foundations of computation and their applications in computer systems
<!--- It is difficult to list a complete range of computer research areas due to their rapid pace of innovation.---> 

## Contains many sub-fields, such as: 

- Computer architecture
- Operating systems
- Computer networking and communication
- Programming methodology and languages
- Algorithm and data structure
- Software engineering
- Database systems
- __artificial intelligence__
- $\ldots$

<https://en.wikipedia.org/wiki/Computer_science>

<!--- 
- parallel computation
- computational complexity theory
- computer graphics

Computer science is a relatively young discipline that begins in the 1940s. It spans theory and practice. It can be seen as a science of problem solving. 
It has strong associations with other disciplines.
Many problems in engineering, science, medicine, agriculture, business, and other fields can be solved effectively with computers. 
The cross-disciplinary knowledge is necessary in order to find a solution.
--->

---

# Turing Machine  (图灵机)

- The **Turing machine** is an **abstract machine** (抽象机器) devised by **Alan Mathison Turing** in 1936  in order to simulate mathematical operation.  
- The foundation of modern computers.

|||
|:---:|:---:|
| <img src="figs/Turing.jpg" alt="Turing" width="230"> | <img src="figs/TuringMachine.jpg" alt="TuringMachine" width="300"> |
|**Alan Mathison Turing**(1912～1954)|**Turing Machine**|

- The **Turing machine** contains: 
a **tape**, a **controller**, and a **read/write head**. 

---

# Turing Machine (cont.)

## Tape
The tape contains several  **discrete cells**, one next to the other. 
Every cell consists of a symbol from the finite alphabet. 
The tape  is infinitely (freely extendable to the right and to the left)  for the  computation. 

## Controller
The controller functionally acts like the **central processing unit (CPU)** in modern computers. Actually, it is a **finite state automaton a machine** that has finite states and can move from one state to another depending on the input. 

## Read/Write head
The read/write head can read and write symbols on the tape and move to the left or to the right one (and only one) cell at a time. In some models the tape moves and the head is stationary, whereas in some models, the head moves and the tape remains stationary. 

<img src="figs/TuringMachine2.png" alt="TuringMachine2" width="400">

<!---
Answer two questions : 
- (1) does a machine exist that can determine whether any arbitrary machine on its tape is "circular" (e.g., freezes, or fails to continue its computational task); 
- (2) does a machine exist that can determine whether any arbitrary machine on its tape ever prints a given symbol.

 and is  Turing shows that a machine with the correct minimal set of operations can calculate anything that is computable, no matter what the complexity is.
Today, the common computer usually has a finite memory, but here we suppose that the Turing machine’s memory is infinite. In this section, we present a very simplified version of the machine to show how Turing machine works.
--->

---

# Von Neumann Model

The **Von Neumann Model (冯•诺依曼模型)** — also known as the ** Von Neumann Architecture** or **Princeton Architecture** — is a computer architecture based on a 1945 description by <mark>Hungarian-American mathematician and physicist **John von Neumann**</mark> and others in <mark>the First Draft of a Report on the **EDVAC (Electronic Discrete Variable Automatic Computer, 离散变量自动电子计算机)**</mark>.

|||
|:---:|:---:|
| <img src="figs/VonNeumann.gif" alt="VonNeumann" width="210">| <img src="figs/EDVAC.jpg" alt="EDVAC" width="350">|
|**John von Neumann**(1903～1957)|**EDVAC**|

---

# Von Neumann Model (cont.)

## TheVon Neumann Model (冯•诺依曼模型)  based on the Turing machine  store data in  memory. 
- **Arithmetic/Logic Unit** (**ALU, 算术逻辑单元**) 
- **Control Unit** (**控制器**) 
- **Memory** (**内存**) 
- **External Storage** (**外部存储器**) 
- **Input(输入) and Output(输出)**

|||
|:---:|:---:|
| <img src="figs/EDVACPlans.jpg" alt="EDVACPlans" width="250">| <img src="figs/VonNeumannArchitecture.png" alt="VonNeumannArchitecture" width="350">|
|**The First Draft Report on the EDVAC(1944)**|**A Von Neumann Architecture Scheme**|

<!---
Computers based on the Turing machine (图灵机) store data(数据) in their memory. Around 1944–1945, John von Neumann proposed that programs (程序) should also be stored in the memory. 

Both data and programs in the von Neumann model have the same logical format. They are stored as binary (二进制) patterns in memory—a sequence of 0s and 1s. 
A program in the von Neumann model contains a finite number of instructions (指令) that are executed sequentially(按顺序执行).
--->

---

# Computer Components

## A computing system contain : 
- **Hardware (硬件)** <br>
Computer hardware is the collection of physical parts of a computer, such as a monitor(显示器),  a graphic card(显卡), a hard disk drive(HDD, 硬盘驱动器) , a sound card(声卡),  memory,  a motherboard(主板),  a mouse(鼠标), a keyboard(键盘), and so on. 

- **Software (软件)** <br>
Computer software is a collection of computer programs, say, operation systems,  procedures, and documentation. 

- **Data (数据)**<br>
 Data are the distinct information with which a computer system deals.

---

# Computer Hardware

## Computer hardware refers to the components that you can physically touch. 

## Installed inside or connected to the outside 
<img src="figs/ComputerHardware.jpg" alt="ComputerHardware" width="250">

- The internal hardware includes CPU, a motherboard, a network card(网卡), a video card(显卡), hard disk drive (HDD, 硬盘驱动器), a solid-state disk (SSD, 固态硬盘), and so on.
- The external hardware includes a flat-panel(平板显示器), a printer(打印机),  a speaker(扬声器), a keyboard, a mouse, a flash memory(闪存), and so on. 

<!---
There are many parts of computer hardware that can be , of a computer
a multi-core processor(多核处理器) a modem(调制解调器), a sound card, a drive (e.g. Blue-Ray(蓝光), CD-ROM(只读光盘驱动器), DVD(数字通用光盘), floppy drive(软盘驱动器),
a projector(投影仪), a scanner(扫描仪),
--->

---

# Computer Software

## Computer software is a collection of programs that a computer executes(执行). 

- The program consists of a sequence of instructions. 
- Each instruction operates on one or more data items. 
- These instructions might be a set of internal system commands(系统命令), or responses to the external input or request. 
- Software tells various hardware components what to do and how to interact with each other. 

<img src="figs/computer_software.jpg" alt="computer_software" width="200">

---

# Computer Software

## System Software(系统软件) 

- System software is used to run hardware, while application software is used to carry out other tasks. 
- The main system software includes **operating systems(操作系统)** and **drivers(驱动程序)**. 

## Application Software(应用软件)

- The main application software includes games, media players, word processors, and so on.
- Software is usually written in high-level programming languages(高级编程语言), which are translated into the **machine language**(**机器语言**) by a **compiler**(**编译器**) or an **interpreter**(**解释器**). 
- Software may also be written in a low-level assembly language(汇编语言) in some dedicated scenarios.

<!---
anti-virus programs(杀毒软件), 
--->

---

# Data

## Data could be <mark> any sequence of symbols having given meaning </mark> by specific actions of interpretation (解释). 
- In daily life, we usually use digits that can take one of ten states ($0$ to $9$). 
However, data stored in a computer generally use only two states ($0$ and $1$).
- Some forms of data (text, image, audio, and video) cannot be stored in a computer directly, and needs to be converted into the **binary** (**二进制**) form ($0$s and $1$s).

## Data can be organized in many types of **data structures** (**数据结构**) such as **arrays** (**数组**), **lists** (**列表**), **graphs** (**图**), and **objects** (**对象**). 
- Modern high performance data persistence (数据持久性) technologies rely on **massively parallel distributed data processing** (**并行分布式数据处理**), such as **Apache Hadoop**. 
- In such systems, the data are distributed across multiple computers and can be processed on different computers at the same time.

---

# Practice Set

## Choice questions :

1. The \_\_\_\_\_\_\_ model is the basic for today's computers. <br>
a) Leibnitz; b) Von Neumann; c) Pascal; d) Charles Babbage

2. In a computer, the \_\_\_\_\_\_\_ subsystem stores data and programs.<br>
a) ALU; b) input\output; c) memory; d) control unit

3. In a computer, the \_\_\_\_\_\_\_ subsystem performs calculations and logical operations.<br>
a) ALU; b) input\output; c) memory; d) control unit

4. In a computer, the \_\_\_\_\_\_\_ subsystem serves as a manager of the other subsystems. <br>
a) ALU; b) input\/output; c) memory; d) control unit

5. According to the Von Neumann model, \_\_\_\_\_\_\_ stored in memory.<br>
a) only data is; b) only programs are; c) data and programs are; d) none of the above

---

# Practice Set (cont.)

## Questions :

1. Explain a computer model based on the Von Neumann architecture.

2. What is the role of a program in a computer based on the Von Neumann model?

3. According to the Von Neumann model, can the hard disk for today be used as imput or output? Explain.

## Note: 
- Please bring your own answer sheet; 
- Please indicat **your name** and **student number** on your answer sheet;
- **Your answer sheet must be submitted after class.**

---

<!---
# History and Development Trends

Computer science has undergone a rapid development since its birth. 
As the field of computer science has emerged, new directions of research and applications have created and combined with classical discoveries in a continuous cycle of growth and revitalization.

Life without a computer is unimaginable. 
The history of computer is an attractive story. 
Computers were not always the brilliant fast machines empowering us to obtain lots of knowledge. Actually, the first computer was very different from the recent computers. 
--->

# Computer History

## The history of the computer can be divided into three periods:

|||
|:---|:---|
| __Mechanical Machines befor 1930__<br> <br> __Electronic Computers from 1930 to 1950__<br> <br> __Computers after 1950__ |<img src="figs/ComputerHis.jpg" alt="ComputerHis" width="250">|

<https://www.worldsciencefestival.com/infographics/a_history_of_computer_science/>

---

#  Mechanical machines

- In the early 17th century, a French mathematician called **Blaise Pascal** invented **Pascaline**, which is a mechanical calculator (机械计算器) performing addition(加法) and subtraction(减法). 
- In the late 17th century, **Gottfried Leibnitz**, a German mathematician, invented **Leibnitz’ Wheel**. 
- In the early 19th century, **Joseph-Marie Jacquard** invented **Jacquard loom**, which adopted the idea of storage and programming at the first time. 
- In the 1820s, **Charles Babbage** invented **Analytical Engine**. 
- In 1890, **Herman Hollerith** invented a programmable machine that could read and sort data on punched cards automatically.

||||||
|:---:|:---:|:---:|:---:|:---:|
|<img src="figs/Pascaline.jpg" alt="Pascaline" width="160">|<img src="figs/LeibnitzWheel.jpg" alt="LeibnitzWheel" width="150">|<img src="figs/JacquardLoom.jpg" alt="JacquardLoom" width="150">|<img src="figs/AnalyticalEngine.jpg" alt="AnalyticalEngine" width="120">|<img src="figs/hollerith_census_machinechm.jpg" alt="hollerith_census_machinechm" width="120">|
|**Blaise Pascal**|**Leibnitz’ Wheel**|**Jacquard loom**|**Analytical Engine**|**Herman Hollerith's invention**|

---

#  Electronic computers

## Between 1930 and 1950, several scientists contributed in the evolution of computer technology who could be considered the true early pioneers of computer science. 

- John Vincent Atanasoff and his assistant Clifford Berry invented the **ABC** (**Atanasoff Berry Computer**) to solve a system of linear equations. It encoded information electrically. 
- In the __1930s__, a huge computer called **Mark I**, was built under the direction of Howard Aiken at Harvard University. 
- In England, Alan Turing invented a computer called **Colossus** to break the German Enigma code. 
- In __1946__, __John Mauchly__ and __J. Presper Eckert__ invented **ENIAC** (**Electronic Numerical Integrator and Calculator**), <mark>the first totally **electronic computer** (**电子计算机**). </mark>
- In 1950, **EDVAC**, <mark>the first computer to implement the stored program concept based on __von Neumann__’s ideas</mark> was built at the University of Pennsylvania.

|||||
|:---:|:---:|:---:|:---:|
|<img src="figs/ABC.jpg" alt="ABC" width="160">|<img src="figs/MarkI.jpg" alt="MarkI" width="160">|<img src="figs/Colossus.jpg" alt="Colossus" width="160">|<img src="figs/ENIAC.jpg" alt="ENIAC" width="160">|
|**Atanasoff Berry Computer**|**Mark I**|**Colossus**|**ENIAC**|

---

#  Computers after 1950

- Between 1950 and 1959, computers were bulky and utilized **vacuum tubes**(**电子管**) as electronic switches. 
- Between 1959 and 1965, **transistors**(**晶体管**) replaced vacuum tubes. Then the size and the cost of the transistorized computers were dramatically reduced. 
- From 1965 to 1985, the appearance of the **integrated circuit**(**IC，集成电路**) further reduced the size and cost of computers, and the microcomputers appeared. 
- Between 1985 and 1995, some advanced computer technology appeared, such as Clusters (集群), Vector Processors (向量处理器), workstations (工作站), minicomputers (小型计算机), laptops (笔记本电脑) and palmtop computers (掌上电脑), and so on. 
- After 1995, high-performance computers (HPC) (高性能计算机) obtained a great advancement, such as supercomputers (超级计算机), many-cores (多核) personal computers (个人电脑), general-purpose graphics processing unit (**GPGPU， 通用计算图形处理单元**), and so on.

<img src="figs/cpu4g.png" alt="cpu4g" width="300">

---

# Development trends

## In the future, computer technology will be characterized by <mark> high performance, miniaturization, network, popularization, intelligence, and humanization. </mark> 
- Lightweight microcomputer <br>
The **lightweight microcomputer**(**轻量级微型计算机**) with small size, low price, powerful function, and high reliability will be popular.
- High performance computer <br>
Development of powerful super computers with high speed, high performance, and capability of processing large and complex problems is also the definite trend. 

---

# Lightweight microcomputer

- A __Pocket PC__ (__掌上电脑__) is a __handheld device__ (__手持设备__) that can be used to process e-mail, play games, exchange messages, browse the Web, and so on. 
- A __laptop computer__ (__笔记本电脑__) has most of the same components into a single unit as a desktop computer, such as a keyboard, a pointing device, a display, and speakers. 
    - Laptop computers have become increasingly popular because they are becoming smaller, lighter, cheaper, and more powerful, and their screens are becoming smaller and of better quality.
- A __smart phone__ (__智能手机__) is based on a mobile operating system such as __Android__ (__安卓__) or __iOS__. 
    - contain high-resolution touch screens (触摸屏), web browsers, global positioning system (GPS) (全球定位系统) navigation (导航) units, and so on.
- An iPad is a kind of __tablet computers__ (__平板电脑__) built on Apple's iOS operating system. 

---

# High performance computer

- A __parallel computer__ (__并行计算机__) has a set of processors that work simultaneously(同时运行). 
    - Parallel computers use multiple computational resources to solve large problems that can often be divided into smaller ones. 
    - Multi-core CPUs and GPUs, the parallel processing is ubiquitous in modern computing. 
- A __supercomputer__ (__超级计算机__) has high-level processing capacity that makes it possible to calculate problems at ultra-high speed. 
    - Supercomputers can be used for highly computationally intensive tasks such as quantum computing(量子计算), weather forecasting, climate research, oil and gas exploration, etc.

<img src="figs/Supercomputers.jpg" alt="Supercomputers" width="350">

---

# Graphics Processing Unit (GPU)

## GPU
- A __graphics processing unit__ (__GPU__, __图形处理单元__) is a specialized electronic circuit used to rapidly handle memory to accelerate the processing of images. 
    - GPU computing utilizes a GPU together with a CPU to accelerate business, scientific and engineering applications. 
    - GPU + CPU is a npowerful union because GPUs consist of thousands of small, efficient cores designed for parallel computing, and CPUs consist of a few cores optimized for serial computing(串行计算). 
    - The __Compute Unified Device Architecture__ (__CUDA__, __统一计算设备架构__) is a parallel computing platform and an __application programming interface__ (__API__, __应用程序编程接口__) model invented by __NVIDIA__. 

<img src="figs/GPU.jpg" alt="GPU" width="300">

---

# Frontiers of Computer Technology

## The frontiers of computer technology include :
- **Supercomputers**
- **Cloud Computing** (**云计算**)
- **Big Data** (**大数据**)
- **Internet of Things** (**物联网**)
- Mobile Computing (移动计算)
- **Quantum Computers** (**量子计算机**)
- Biocomputers (生物计算机)
- **Service-Oriented Architecture** (**SOA，面向服务的体系结构**)
- Modern Artificial Intelligence(现代人工智能技术) 
- etc.

<!---
- Virtualization (虚拟化技术), 
- Visualization(可视化技术)，
--->

---

#  Supercomputer

## A supercomputer is a computer that performs calculation at the currently highest operational rate. 

<!---It is typically used for scientific and engineering applications that deal with very large databases or do large amounts of computation (or both). 
Figure 1.2 shows that supercomputing has increasingly become the cornerstone of modern society.
--->
- Supercomputers play an important role in the field of computational science. 
<!---
The stages of supercomputer application.
include simulation(仿真) and modeling(建模), weather forecasting, meteorology(气象学), geological exploration(地质勘探), cryptography (密码学) (encryption (加密) and decryption (解密)), virtual reality (虚拟现实), visualization(大规模场景的可视化), artificial intelligence(人工智能), nuclear weapons development (核武器开发) , precise missile guide (精确制导), long-range attack(远程打击), quantum simulation(量子模拟), novel drug synthesis and discovery(新型药物的合成和发现), novel material synthesis(新材料的合成), space explorations(太空探索), data mining (数据挖掘), business intelligence, etc. 
Supercomputers can be applied to calculate the structures and properties of chemical compounds(化合物), biological macromolecules(生物大分子), polymers(聚合物), and crystals(晶体). High performance supercomputers are widely employed in physical simulations, such as simulation of airplanes in wind tunnels(风洞), simulation of the detonation(爆炸) of nuclear weapons, and research into nuclear fusion(核聚变).
--->

## Sunway TaihuLight (神威•太湖之光)
- According to the 47th edition of the TOP500 list of the world’s most powerful supercomputers announced in June 2016, maintained his No. 1 position  built entirely using China designed and made processors. 
- $93$ __petaflop/s__ (__quadrillions of calculations per second, 每秒1千万亿次运算__) on the __LINPACK__ benchmark.
<!---
Developed by the National Research Center of Parallel Computer Engineering & Technology (NRCPC) and installed at the National Supercomputing Center in Wuxi, Sunway TaihuLight displaces Tianhe-2 (Milkyway-2)(天河二号), an Intel-based Chinese supercomputer that has retained the No. 1 position with 33.86 petaflop/s on the past six TOP500 lists. Table 1.1 shows the top 10 sites for June 2016.
--->

<img src="figs/Supercomputers.jpg" alt="Supercomputers" width="350">

---

# Cloud Computing

## Cloud computing is a model for enabling ubiquitous, convenient, on-demand(按需所选) network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services)
<!---
according to the NIST (National Institute of Standards and Technology) definition. 
Cloud computing has become one of the most powerful and economical paradigms in terms of technology, architecture, and IT services for performing complex computations in large-scale scientific and business applications. 
A great number of organizations have been shifting to cloud computing environment. 
--->

- The benefits of cloud computing include virtualized resources(虚拟化的资源), elasticity (自由伸缩性), scalability (可扩展性), flexibility (灵活性) of services, on-demand delivery of resources, efficiency, parallel processing, cost saving, and a lot more. 

- Cloud computing is a form of utility computing (效用计算) where IT resources are delivered on a Pay-As-You-Use (使用才支付) basis, just as electricity is charged based on usage.

<!---
Using cloud computing, large organizations can process their large-scale jobs more quickly, since using hundred servers per hour outweighs the benefits than using one server for hundred hours. 
In cloud computing, users can ubiquitously run applications, and store/access their data on an off-site, location-transparent(位置透明), centrally managed, shared platform. The resources provided by cloud are usually run on virtual machines (虚拟机) paralleled with the physical infrastructure. 
--->

<img src="figs/CloudComputing.png" alt="CloudComputing" width="250">

---

# Cloud Computing

##  public cloud computing types :  
- __Infrastructure as a Service (IaaS, 基础设施即服务)__
- __Platform as a Service (PaaS, 平台即服务)__
- __Software as a Service (SaaS, 软件即服务)__
- __Data as a service (DaaS, 数据即服务)__ 
- so on. 

## The distributed cloud computing is much more affordable and scalable than the supercomputer. 
- The processing power of cloud computing grows as additional servers (with their processors) are added to the network. 

<!---
On the other hand, supercomputers have the advantage of sending data through fast connections, while cloud computing architecture sends data through slower networks.

A supercomputer consists of the best processors, rapid memory, specially designed components, and elaborate cooling mechanisms, so it is not easy to scale a supercomputer. 
--->

---

# Big Data

<!---
Data, structured or unstructured, produced by organizations, Internet of Things (IoT) (物联网) and social media is growing tremendously. 
This fast and sudden growth of big data requires fast development of big data technologies through virtualization platforms. 
- The terms __volume__, __variety__, and __velocity__ were initially presented by __Gartner__ to describe challenges of big data. 
--->
## __Big data__ refers to the large increase in the volumes of data that needed advanced technologies and techniques to capture, store, process, distribute, manage and analyze the information. 
- the elements of big data are characterized by __4Vs__:  <mark>__V__olume (容量大), __V__ariety (种类多), __V__elocity (要求处理速度快), and __V__alue (密度低，但价值高).</mark>

    - __Volume__ refers to the continuously expanding magnitude of all types of data produced from various sources, such as IoT, social media, multimedia, and a lot more. 
    - __Variety__ refers to the various structures of data gathered through IoT, social networks, smart devices, or sensors. 
    - __Velocity__ refers to the rate of data generation and speed of data transfer and analysis. 
    - __Value__ is very crucial characteristic of big data. 

<!---
It is the process of rapidly determining hidden patterns or valuable information from various types of big data.

IT organizations want to take advantage of cloud computing architecture to support big data projects. 
Cloud computing provides enterprises cost-effective, flexible access to big data’s huge volumes of information. 
Meanwhile big data on the cloud generates plentiful on-demand computing resources. Both cloud computing and big data technologies will continue to evolve and congregate in the future.
<img src="figs/BigData3.jpg" alt="BigData" width="150">
--->

---

# Internet of Things

## The __Internet of Things__, or __IoT__, is a network of items, each embedded with sensors (传感器), which are connected to the Internet. 
- IoT is defined as the worldwide dynamic global autonomous network of interconnected physical or virtual things, devices or objects based on standard network protocols (网络协议). 
- IoT refers to an emerging paradigm consisting of a continuum of uniquely addressable things communicating with one another to form a worldwide dynamic network.
<!--- - Nowadays, many smart devices(智能设备) are connected to the Internet; smart buildings have multiple sensors to protect them from disasters or accidents and to save energy; and smart devices support various fields including healthcare services, business, education, and industry. 
Huge volumes of data and information are generated by these devices, which are connected directly or indirectly via Internet. 
--->
- Cloud based platforms and applications help to connect objects in IoT at any place and at any time. 
Therefore, the front end to access IoT is the cloud. 
<!---
Cloud provides the needed __infrastructure__ (__基础设施__), computation powers, storage and applications to interact with smart devices in real-time.
The huge amounts of data produced from the connections of devices in IoT can only be captured, processed, stored and transformed into valuable information through clouds. 
Clouds provide physical and virtual systems, applications and tools to efficiently and intelligently process and analyze big data and IoT.
--->

<img src="figs/IOT.jpg" alt="IOT" width="350">

---

# Mobile Computing

## Mobile computing is a technology that allows transmission of data, via a computer or any other wireless device without having to be connected to a fixed physical link. 
- Mobile computing involves mobile communication(移动通信), mobile hardware, and mobile software. 
- Mobile communication issues include ad-hoc (点对点) and __infrastructure networks__ (__基础设施网络__), communication properties, protocols (协议), data formats and concrete technologies, etc. 
- Hardware includes mobile devices or components. 
- Mobile software handles the characteristics and requirements of mobile applications. 
- One of the most important characteristics of mobile computing is __portability__. 

---

# Quantum Computer

## A __quantum computer__ (__量子计算机__) makes direct use of quantum mechanical phenomena, such as superposition (叠加) and entanglement (纠缠), to perform calculations. 
- Quantum computation uses __quantum bits__ (__量子比特__), which can be in <mark>superpositions of states</mark>. 
- Quantum computers have the ability to be in multiple states simultaneously. 
    - Large-scale quantum computers may theoretically be able to solve certain problems asymptotically faster than any conventional computer by using the best algorithms, such as integer factorization(整数分解) using __Shor's algorithm__ (__秀尔算法__).

<img src="figs/QuantumComputer.jpg" alt="QuantumComputer" width="300">

<!---
- Quantum computers are different from digital computers based on transistors. 
- Quantum computation makes use of quantum properties to represent data and perform operations on data, while digital computers require data to be encoded into binary digits. 
--->

---

# Biocomputer

## __Biocomputers__ (__生物计算机__) use biologically derived materials, such as DNA and proteins(蛋白质), to perform computational functions. 
- Currently, biocomputers have various functional capabilities, such as operations of binary logic and mathematical calculations. 
- Three typical types of biocomputers include biochemical computers, biomechanical computers, and bioelectronic computers. 
- In the future, biocomputers can obtain a long-term development by the expanding new science of __nanobiotechnology__ (__纳米生物技术__). 

<img src="figs/Biocomputer.png" alt="Biocomputer" width="400">

---

# Virtualization

## Virtualization(虚拟化) is the simulation of the software or hardware upon which other software runs. 
- It creates virtualized components including hardware platforms, operating systems (OS), storage devices, and network devices, etc. 
- Based on virtualization technology, the IT environment will be able to manage itself based on perceived activity, and utility computing. 
- Virtualization is aimed to centralize administrative tasks, improve scalability and overall hardware-resource utilization. 
- Virtualization reduces overhead costs due to parallelism of operating systems on a single central processing unit. 
- Using virtualization, an enterprise can better control updates of the operating system and applications without disrupting users.

<img src="figs/Virtualization.png" alt="Virtualization" width="400">

---

# Service-Oriented Architecture (SOA)

## A **service-oriented architecture** (**SOA**，**面向服务的体系结构**) is a set of methodologies for designing software in the form of interoperable services(可互操作的服务). 
- These services can provide the functionalities of large software applications that can be reused whenever needed. 
- Service-orientation needs loosely coupled (松耦合) services between operating systems and other technologies that underlie applications. 
    - <mark>Services are independent of any other vendor, product, service, or technology</mark>. 
    - Provide services to other components via a communication protocol, mostly over a network.

<img src="figs/soa.png" alt="SOA" width="200">

---

#  Major Fields of Computer Science

## Mathematical foundations
mathematical logic (数理逻辑), set theory (集合论), number theory (数论), graph theory (图论), category theory (范畴论), numerical analysis (数值分析), information theory (信息论)

## Theory of computation(计算理论)
automata theory (自动机理论), computability theory (可计算性理论), computational complexity theory (计算复杂性理论), quantum computing theory, 
**Algorithms**(**算法**) and **data structures**(**数据结构**),
analysis of algorithms, algorithm design, computational geometry (计算几何)

## System architecture
**digital logic** (**数字逻辑**), memory systems, computer architecture, computer organization, operating systems
Concurrent (并发), parallel (并行), and distributed systems (分布式系统),
multiprocessing (多重处理), grid computing (网格计算), concurrency control,
Programming languages and compilers(编译器),
parsers (解析器), interpreters, procedural programming, object-oriented programming, functional programming, logic programming

---

#  Major Fields of Computer Science

## Software engineering(软件工程)
requirements analysis, software design, computer programming, formal methods, software testing, software development
Databases(数据库),
data mining, relational databases (关系型数据库), online analytical processing (OLAP) (联机分析处理), distributed and parallel database systems, database security (安全) and privacy (机密性),

## Computer graphics(计算机图形学) and visual computing
visualization (可视化), image processing (图像处理), advanced geometric modeling (几何建模), mainstream rendering (主流渲染) techniques, computer animation (计算机动画),
Human computer interaction (人机交互),
computer accessibility (可访问性), user interfaces (用户接口), wearable computing (可穿戴计算), ubiquitous computing (普适计算), virtual reality, multimedia (多媒体),
Telecommunication(通信) and networking,
routing(路由), network topology (网络拓扑结构), cryptography(密码学), security and privacy

---

#  Major Fields of Computer Science

## Artificial intelligence(人工智能)
automated reasoning (自动推理), computational linguistics (计算语言学), computer vision (计算机视觉), evolutionary computation (进化计算), **machine learning** (**机器学习**), **neural networks** (**神经网络**), natural language processing (自然语言处理), **robotics** (**机器人学**)

## Scientific computing
artificial life (人工生命), bioinformatics (生物信息学), cognitive science (认知科学), computational chemistry (计算化学), computational neuroscience (计算神经科学), computational physics (计算物理学), **numerical algorithms** (**数值算法**), symbolic mathematics (符号数学)

---

# Practice Set

## Questions :

1. What is supercomputer? Which supercomputer is the new No.1 system?
2. What is cloudcomputing? What are the characteristics of cloud computing? 
3. What are the characteristics of big data?
4. What is the definition of IoT?
5. What are the major research fields of computer science? Explain.

## Note: 
- Please bring your own answer sheet; 
- Please indicat **your name** and **student number** on your answer sheet;
- **Your answer sheet must be submitted after class.**

---

# Summary

- Computer science deals with the study and the science of the theoretical foundations of information and computation and their implementation and application in a wide variety of computer systems.
- The von Neumann architecture has four subsystems: memory, arithmetic logic unit, control unit, and input/output. The von Neumann model states that <mark>the program instructions and data must be stored in main memory.</mark>
- We can conceptualize a computer as being made up of three important components: **computer hardware**, **computer software**, and **data**.
- In general, the history of computing and computers can be classified into three periods: the period of **mechanical machines** (before 1930), the period of **electronic computers** (1930-1950), and the period after generations (1950-present).
- In the future the development of computer technology will represent miniaturization, high performance, network, popularization, intelligence and humanization.

---

# Summary (cont.)

- The frontiers of computer technology include **supercomputer**, **cloud computing**, **big data**, **Internet of Things**, mobile computing, **quantum computer**, biocomputer, virtualization, **service-oriented architecture (SOA)**, and so on.
- The major fields of computer science include **mathematical foundations**, **theory of computation**, **algorithms** and **data structures**, system architecture, parallel and distributed systems, **programming languages** and compilers, software engineering, databases, **artificial intelligence**, computer graphics, human computer interaction, telecommunication and **networking**, scientific computing, and so on.

---

# Homework

- In addition to the **Von Neumann architecture**, do you know other types of computer architecture?
    - Key word: **computer architecture**, **Von Neumann**

- In addition to the Turing machine, there is also a well-known **Turing test** in the field of artificial intelligence. Explain its principle?
    - Key word: **Turing test**

---

#  References

- Behrouz A. Forouzan and Firouz Mosharraf: Foundations of Computer Science, second edition, London: Thomson Learning, 2008.
- Schneider GM and Gersting JL: Invitation to Computer Science, Boston, MA: Course Technology, 2004.
- Dale N and Lewis J: Computer Science Illuminated, Sudbury, MA: Jones and Bartlett, 2004.
- Patt Y and Patel S: Introduction to Computing Systems, New York: McGraw-Hill, 2004.
Allen B. Tucker and Peter Wegner: Computer Science Handbook, second edition, Chapman and Hall/CRC, 2004.
- ACM/IEEE-CS Joint Task Force. Computing Curricula 2001, Computer Science Volume. ACM and IEEE Computer Society, December 2001. (<http://www.acm.org/sigcse/cc2001>)
- <http://www.nvidia.co.uk/object/tesla-high-performance-computing-uk.html>
- <http://www.nvidia.com/object/cuda_home_new.html>
- <http://www.top500.org/>

---

#  References (cont.)

- Armbrust M, Fox A, Griffith R, Joseph AD, Katz R, Konwinski A, and Zaharia M: A view of cloud computing. Communications of the ACM, 53(4), 50-58, 2010.
- Gantz J, Reinsel D: Extracting value from chaos, IDC iView, 1–12, 2011.
- Gandomi A and Haider M: Beyond the hype: Big data concepts, methods, and analytics. International Journal of Information Management, 35(2), 137–144, 2015.
- Gubbi J, Buyya R, Marusic S and Palaniswami M: Internet of Things (IoT): A vision, architectural elements, and future directions. Future Generation Computer Systems, 29(7), 1645-1660, 2013.


<!---

# Practice Set

Please Submit your completed homework:
for Civil Engineering, Elite [ei'li:t; ɪ'li:t] and Selected Students (must complete all taught & numbered practice sets, 所有练习题都要做)
	to  ….
for Finance, Environmental Engineering , and Foreign Students (must complete all taught & numbered practice sets, 所有练习题都要做) 
	to  ….

--->

<!---
landslide file.md -i -m -o > file.html
landslide file.md -i -x tables -m -o > file.html
--->
