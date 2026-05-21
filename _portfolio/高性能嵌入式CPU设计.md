---
title: "高性能嵌入式CPU设计"
excerpt: "围绕 CPU 设计的项目记录"
collection: portfolio
---



## 高性能嵌入式RISC-V CPU设计与验证   

- 完整RV32IMF指令集
  - 除基本运算访存指令还包含FENCE、CSR、ECALL、EBREAK等特殊指令
  - CSR与特权级支持：最小 M-mode 特权支持，通过CSR指令读改写必须的CSR。
- 高性能前端
  - 高性能IFU：通过request FIFO、response FIFO 解耦请求发射与响应消费
  - IF和ID间设计4-entry 的 Fetch Queue
- 

