---
title: AI-DaaS
subtitle: 基于Kubernetes弹性部署人工智能/机器学习(AI/ML)模型到生产环境
layout: product
image: /img/daas-design.jpg
features:
    - label: 利用Kubernetes提供可靠且可扩展的部署服务
      icon: fa-circle
    - label: AI/ML模型的自动化部署系统，支持传统数据挖掘模型和深度学习模型
      icon: fa-circle
    - label: 部署完整的Pipelines (数据预处理 -> 模型预测 -> 预测值后处理)，而不仅仅是模型本身
      icon: fa-circle
    - label: 支持在本地私有或公有云中的Kubernetes上部署
      icon: fa-circle
redirect_from: 
    - /products/ai-daas
---
<h4>AI-DaaS简介</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      AI-DaaS是一套基于Kubernetes的人工资能/机器学习（AI/ML）自动部署系统，提供一键式自动部署开源模型到生产环境中，支持PMML，Scikit-learn，XGBoost，LigthGBM，Spark ML和目前主流深度学习框架ONNX，TensorFlow，Keras，Pytorch，MXNet等，以及用户自定义模型的部署。
    </p>
    <p>
      伴随开源技术的进步，数据分析师现在可以很容易的训练模型，比如在自己的电脑上安装Anaconda包，启动Jupyter notebook，使用Numpy和Pandas预处理数据，调用XGBoost或者LightGBM可以很容易的训练一个精度不错的模型。但是因为生产环境和开发环境的不同，模型的部署却不是那么容易，一些常见的问题包括：如何能同时部署数据预处理和模型本身，如何为预测推断提供REST API，如何调试REST API，如何管理模型，如何无缝切换模型版本，如何监控部署性能，如何弹性扩展部署服务，如何能批量预测并且支持不同的数据源，如何进行模型评估等等，这些问题都可以在AI-DaaS系统中找到答案。
    </p>
    <p>
    AI-DaaS使用项目来管理用户的数据分析工作，用户可以为不同的任务创建不同的项目，在项目中可以管理各种分析资产，包括模型、部署、脚本、数据、数据源等，图一为项目首页仪表盘：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-dashboard.jpg" alt="项目仪表盘" />
      <p>图一（项目仪表盘）</p>
    </figure>
  </div>
</div>
<h4>部署完整Pipelines，而不仅仅是模型本身</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      AI-DaaS支持部署Pipelines，而不仅仅是模型本身。AI-DaaS基于函数即服务（Function-as-a-Service）构建，自动为多种编程语言函数生成REST API。在AI-DaaS中，用户可以很容易创建包含了模型预测功能的程序脚本，基于该脚本，用户可以自由添加数据预处理或者预测值后处理的函数或者代码，满足用户各种自定义功能。以AI开发语言Python为例，下图二是AI-DaaS自动生成的用户自定义预测脚本：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-custom-scoring.jpg" alt="自定义预测脚本" />
      <p>图二（自定义预测脚本）</p>
    </figure>
  </div>
</div>
<h4>提供开发测试和正式部署两种模式</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      AI-DaaS提供两套API，分别针对开发和产品模式，用户可以在图二界面中使用开发API来测试添加的功能，测试完成后，再创建正式的网络部署，上线完整的Pipelines, 或者使用任意的REST客户端来测试，关于API信息，可以点击命令“生成代码”来获取，图三所示：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-generate-code.jpg" alt="测试API" />
       <p>图三（测试API）</p>
    </figure>
  </div>
</div>
<h4>支持主流开源模型</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      借助于AI-DaaS Web界面可以直接部署PMML和ONNX模型，或者DaaS-Client客户端（目前支持Python）部署其他基于Python主流开源模型：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-models.jpg" alt="模型列表" />
      <p>图四（模型列表）</p>
    </figure>
  </div>
</div>
<h4>管理模型不同版本</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      支持添加和管理模型的不同版本:
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-model-overview.jpg" alt="模型概述" />
      <p>图五（模型概述））</p>
    </figure>
  </div>
</div>
<h4>监控部署服务</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      监控部署性能，提供各种网络服务性能指标：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-service.jpg" alt="" />
      <p>图六（网络服务部署）</p>
    </figure>
  </div>
</div>
<h4>部署服务资源分配</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      支持自由切换部署的模型版本，提供网络负载，增加或者减少部署副本量，弹性扩展部署服务：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-edit-service.jpg" alt="更新网络服务部署" />
      <p>图七（更新网络服务部署）</p>
    </figure>
  </div>
</div>
<h4>部署任务批量预测和模型评估</h4>
<div class="columns">
  <div class="column is-8">
    <p>
      除了支持部署网络服务，AI-DaaS还可以部署任务，用户可以在任务中执行任何自定义操作。AI-DaaS支持生成批量预测和模型评估的脚本，用户可以通过部署任务来执行：
    </p>
  </div>
  <div class="column is-4 has-text-centered">
    <figure class="image">
      <img src="/img/daas-job.jpg" alt="任务部署" />
      <p>图八（任务部署）</p>
    </figure>
  </div>
</div>
<div class="buttons is-centered">
  <a href="/about" class="button is-info">申请体验</a>
</div>
