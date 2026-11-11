## Hi there! 👋

I'm Ankit, a Solutions Architect/Technical Product Manager based in San Francisco. I build AI agents, take them to production, and write about what breaks along the way.

For more than ten years at Sumo Logic, I worked with enterprise customers and owned our technical partnerships with AWS, Google Cloud, and Azure. I ran POCs, designed reference architectures, and led an [industry-first set of 11 Google Cloud integrations](https://www.sumologic.com/blog/google-cloud-platform-apps). Most recently I built AI agents for security and reliability work: a SOC triage agent on Amazon Bedrock that cut manual triage time by about 60%, and a multi-agent SRE investigation system that went into beta with enterprise customers.

I care most about the gap between a good demo and a system people can trust: evals, guardrails, cost per task, and the inference stack underneath. I learn by building, measuring, and writing up what I find, including the parts that didn't go as expected.

### Current Focus

- Memory for long-running agents: short-term vs. long-term, and semantic, episodic, and procedural memory for an on-call SRE agent
- LLM inference: how serving optimizations like continuous batching, prefix caching, and speculative decoding actually behave on real workloads
- Securing agents: prompt injection, least-privilege tools, and human approval that can't be bypassed

### What I've Built

**[agentic-ai](https://github.com/ankitgoelcmu/agentic-ai)**: agent patterns and end-to-end projects, each with its own README.

*Patterns*, the building blocks:
- [Prompt chaining](https://github.com/ankitgoelcmu/agentic-ai/tree/main/patterns/prompt_chaining): breaking a task into fixed, checkable steps (design to code)
- [Routing](https://github.com/ankitgoelcmu/agentic-ai/tree/main/patterns/routing): sending each request to the right specialist
- [Parallelization](https://github.com/ankitgoelcmu/agentic-ai/tree/main/patterns/parallel): running independent checks at the same time (security checks)
- [Orchestrator-workers](https://github.com/ankitgoelcmu/agentic-ai/tree/main/patterns/worker_orchestrator): one agent planning and delegating to others (stock research)
- [Evaluator-optimizer](https://github.com/ankitgoelcmu/agentic-ai/tree/main/patterns/eval_optimizer): one model drafts, another critiques, until it passes

*Projects*, the patterns applied:
- [Agent guardrails](https://github.com/ankitgoelcmu/agentic-ai/tree/main/examples/guardrails_demo): a real prompt injection fools the model and still goes nowhere, because of how the system is built
- [CyberGuard](https://github.com/ankitgoelcmu/agentic-ai/tree/main/examples/sigma_rule_writer): a multi-agent system that turns threat intel reports into validated Sigma detection rules
- [SOC triage on Databricks](https://github.com/ankitgoelcmu/agentic-ai/tree/main/examples/databricks_soc_triage): governed agent tools and an MLflow comparison of open-weight models, where the smallest model beat the largest
- [Async subagents](https://github.com/ankitgoelcmu/agentic-ai/tree/main/examples/async_agent): the user changes their mind mid-task, and the agent switches course without making them wait (LangChain async subagents)
- [vLLM inference lab](https://github.com/ankitgoelcmu/agentic-ai/tree/main/examples/vllm_inference_lab): four serving optimizations measured on one GPU. Prefix caching made the first token 9x faster for agent-style prompts

**[DeepLearning](https://github.com/ankitgoelcmu/DeepLearning)**: my notebooks from learning deep learning from the ground up in PyTorch, including a GPT-2 style language model, a Vision Transformer replicated from the paper, and QLoRA fine-tuning of BERT for network threat detection.

### Some of My Recent Articles

*I write about AI agents in production, security, and LLM inference, always with the code and numbers behind it.*

- [Speculative Decoding, Disaggregation, and How to Pick the Right LLM Inference Optimizations](https://medium.com/gitconnected/speculative-decoding-disaggregation-and-how-to-pick-the-right-llm-inference-optimizations-081c110cd3d3)
- [FlashAttention, Prefix Caching and Continuous Batching: How LLM Servers Keep the GPU Busy](https://medium.com/gitconnected/flashattention-prefix-caching-and-continuous-batching-how-llm-servers-keep-the-gpu-busy-3855fc1784f6)
- [Why LLM Inference Is Slow: Prefill, Decode and the KV Cache](https://medium.com/gitconnected/why-llm-inference-is-slow-prefill-decode-and-the-kv-cache-401c9fb743bb)
- [Agent Memory: What to Keep, Where to Keep It, and When to Read It](https://medium.com/gitconnected/agent-memory-what-to-keep-where-to-keep-it-and-when-to-read-it-1cdfecb455be)
- [How to Evaluate AI Agents: A Practical Guide](https://medium.com/gitconnected/how-to-evaluate-ai-agents-a-practical-guide-8d5d6378d6de)
- [Your Agent Can Talk While It Works: Testing LangChain's Async Subagents](https://medium.com/gitconnected/your-agent-can-talk-while-it-works-testing-langchains-async-subagents-474ab1c85882)
- [Your RAG Is Only as Good as Your OCR](https://ankitgoelcmu.medium.com/your-rag-is-only-as-good-as-your-ocr-7b2100bffd9f)
- [Why RAG Still Hallucinates, and What Advanced RAG Fixes](https://ankitgoelcmu.medium.com/why-rag-still-hallucinates-and-what-advanced-rag-fixes-fd66f40008f5)
- [Your RAG Works in the Demo. Here's Why It Fails in Production.](https://ankitgoelcmu.medium.com/your-rag-works-in-the-demo-heres-why-it-fails-in-production-0721c7e713f3)
- [An AI Just Edited Another AI's Brain. No Training Required.](https://ankitgoelcmu.medium.com/an-ai-just-edited-another-ais-brain-no-training-required-eae29176d031)
- [Your AI Agent Is Only as Reliable as Its 60th Tool Call](https://medium.com/@ankitgoelcmu/your-ai-agent-is-only-as-reliable-as-its-60th-tool-call-e9cc79a73e8a)
- [How to Read an AI Agent Trace](https://ankitgoelcmu.medium.com/how-to-read-an-ai-agent-trace-fab8e8391506)
- [What Happens When an LLM Guesses Ahead](https://ankitgoelcmu.medium.com/what-happens-when-an-llm-guesses-ahead-70514d25164d)
- [How vLLM Stops Wasting GPU Memory](https://ankitgoelcmu.medium.com/how-vllm-stops-wasting-gpu-memory-f4d31da91bba)
- [What Happens When 64 Users Share One GPU](https://ankitgoelcmu.medium.com/continuous-batching-measured-why-one-gpu-can-serve-64-users-200b9e0246b6)
- [Guardrails for AI Agents: What Actually Enforces Them](https://ankitgoelcmu.medium.com/guardrails-for-ai-agents-what-actually-enforces-them-fbf6c6f5f8cf)
- [What Actually Breaks When You Deploy an AI Agent](https://ankitgoelcmu.medium.com/what-actually-breaks-when-you-deploy-an-ai-agent-d8f2457e2d94)
- [The Detection Gap: Why AI-Powered Attacks Are Outrunning Our Defenses](https://ankitgoelcmu.medium.com/the-detection-gap-why-ai-powered-attacks-are-outrunning-our-defenses-and-how-im-closing-it-63b75e392def)

▶️ You can read all my posts on [Medium](https://medium.com/@ankitgoelcmu).

### Tools I Use

LangChain · LangGraph · MCP · PyTorch · Hugging Face · vLLM · MLflow · LangSmith · Amazon Bedrock · Databricks · AWS · GCP · Azure · Docker · Kubernetes · Terraform

### Let's Connect

I'm currently open to Solutions Architect, Technical Product Manager, Customer Engineer, and Forward Deployed Engineer roles in AI. I'm always happy to talk about agents, inference, or getting AI past the demo stage.

[LinkedIn](https://www.linkedin.com/in/ankitgoe/) · [Medium](https://medium.com/@ankitgoelcmu) · ankitgoel.cmu@gmail.com
