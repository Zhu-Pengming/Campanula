# Campanula
A project combining hardware and software that involves natural language processing

番茄植物（Tomato Plant）：对环境变化敏感，易于观察其反应。

# Project Florence 模块划分

## 1. 硬件模块
- **3D 打印底座**：设计并打印用于容纳植物和传感器的基座。
- **定制玻璃碗**：制作一个适合底座的玻璃碗用于放置植物。
- **传感器组件**：包括空气温度传感器、土壤湿度传感器、一氧化碳水平传感器、湿度传感器。
- **LED 灯环**：控制红色和蓝色光频用于与植物互动。
- **微型打印机**：用于打印植物的回应。
- **Arduino 微控制器**：两个 Arduino 微控制器用于读取传感器数据并控制其他硬件。

## 2. 软件模块
- **传感器数据采集和处理**：编写 Arduino 程序读取传感器数据并发送至 Azure 云服务。
- **自然语言处理（NLP）**：在 Azure 云服务中使用 NLP 分析用户输入的情感和句子结构，并将其翻译成植物可以理解的光信号。
- **植物回应生成**：基于传感器数据和用户输入生成植物的回应，并通过微型打印机打印出来。

## 3. 云服务模块
- **数据存储和处理**：在 Azure 上创建服务用于存储和处理传感器数据和用户输入。
- **情感分析**：利用 Azure 的 NLP 服务分析用户输入的情感并决定光信号的频率和持续时间。
- **响应生成**：根据情感分析结果和植物的当前状态生成适当的回应。

## 4. 用户界面模块
- **输入界面**：在 Microsoft Surface 平板上创建用户界面，让用户可以输入消息与植物互动。
- **显示和反馈界面**：显示用户输入的情感分析结果和植物的回应。

# Project Florence 模块划分和开发顺序

## 1. 硬件模块
先搭建硬件部分，因为这部分的准备工作是整个项目的基础。

### 步骤：
1. **3D 打印底座**：
   - 设计一个能够容纳植物、传感器、LED 灯环和微型打印机的底座。
   - 使用 3D 打印机打印设计好的底座。

2. **定制玻璃碗**：
   - 制作一个适合底座的玻璃碗，用于放置植物。

3. **传感器组件**：
   - 准备空气温度传感器、土壤湿度传感器、一氧化碳传感器和湿度传感器。
   - 连接传感器到 Arduino 微控制器。

4. **LED 灯环**：
   - 准备 LED 灯环，连接到 Arduino 微控制器，确保能够控制红色和蓝色光频。

5. **微型打印机**：
   - 准备微型打印机并连接到 Arduino 微控制器。

6. **Arduino 微控制器**：
   - 准备两个 Arduino 微控制器，连接所有传感器和输出设备。

## 2. 软件模块
在硬件部分搭建完毕并能够正确工作后，进行软件开发。

### 步骤：
1. **传感器数据采集和处理**：
   - 编写 Arduino 程序读取传感器数据并通过串口发送到计算机或云服务。

2. **自然语言处理（NLP）和植物回应生成**：
   - 开发用于处理用户输入的程序，将输入发送到 Azure NLP 服务进行情感分析，并将分析结果转换为光信号。

## 3. 云服务模块
在本地软件模块开发完成并测试后，开始配置和开发云服务部分。

### 步骤：
1. **数据存储和处理**：
   - 在 Azure 上创建存储和处理传感器数据和用户输入的服务。

2. **情感分析**：
   - 使用 Azure 的 NLP 服务分析用户输入的情感并决定光信号的频率和持续时间。

3. **响应生成**：
   - 根据情感分析结果和植物的当前状态生成适当的回应，并通过微型打印机打印出来。

## 4. 用户界面模块
硬件和软件部分完成后，开发用户界面模块以实现用户与植物的互动。

### 步骤：
1. **输入界面**：
   - 在 Microsoft Surface 平板上创建用户界面，让用户可以输入消息与植物互动。

2. **显示和反馈界面**：
   - 显示用户输入的情感分析结果和植物的回应。

## 建议：
- **先进行硬件模块的搭建和测试**，确保所有传感器和输出设备都能正确工作。
- **然后进行软件模块的开发**，从传感器数据采集开始，逐步增加功能。
- **接着开发云服务模块**，将本地处理迁移到云端，以提高系统的扩展性和稳定性。
- **最后开发用户界面模块**，完善用户交互体验。





