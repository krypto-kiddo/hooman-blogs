
---
Everything a Dev Needs to Know about Serverless Architecture<br>
<sub><span style="color: grey; font-size: 80%;">29 Sept 2023, Yashwardhan Dixit</span></sub>
---

![Cover Image](https://i.imgur.com/yCsUTjH.jpeg)

Since the 1960s, cloud computing has revolutionized the way we manage and scale our resources. It has given us the power to access new servers and explore advanced platform services, including API gateways, queues, and authentication mechanisms. But what about serverless computing? Many tend to associate serverless with Functions-as-a-Service (FaaS) products, and due to disappointments in this domain, they often overlook the broader concept of serverless. If you're reading this, you have a more open perspective.

### Understanding Serverless
At its core, serverless computing is defined by two key features: the absence of visible infrastructure, replacing configured VM images, and billing based on function invocation rather than traditional hourly fees. It's not as nebulous as it may seem; in fact, a significant portion of cloud services is already serverless. The crux of the issue that makes some developers uneasy is the idea of their code being serverless. How can they debug and monitor this environment? Is "serverless" merely an evolution of Platform as a Service (PaaS) and Infrastructure as a Service (IaaS), or is it a paradigm shift?

Serverless? But the code has to run somewhere.
True, the hardware still exists. When we say "serverless," it's essentially a level-of-service abstraction, designed for the developer's convenience. Serverless architecture shifts the responsibility for managing the environment from the user to the cloud provider, offering a compelling reason to embrace this assistance. With serverless, the service provider takes full responsibility for managing and provisioning infrastructure, allowing developers to focus exclusively on writing code.

In a traditional approach, developers need to handle installing, running, monitoring, and updating services that communicate within the system, all running on virtual machines. In a serverless approach, the service provider handles everything, from processes to operating systems to servers. This means you no longer need to purchase dedicated servers, while the service provider can efficiently serve requests from all clients.
<hr>

### BaaS and FaaS
Serverless architecture can be viewed as an evolution of Platform-as-a-Service (PaaS). In a serverless setup, applications rely on either third-party services known as Backend as a Service (BaaS) or custom code executed in ephemeral containers via Function as a Service (FaaS).

#### BaaS
With the increasing availability of third-party service providers offering required functionality and managing their internal states, applications have transitioned to rely on these services, eliminating the need for application-specific server-side logic. In this context, these applications are considered serverless.

#### FaaS
Notably, AWS Lambda and Azure Functions were among the pioneers of serverless computing. These services host code snippets that execute on demand. Instead of creating entire applications, you create modular code pieces triggered by event rules. You don't have to worry about the underlying server, and you're billed according to usage metrics like memory and CPU. The scalability is seamless, whether you have one or a million invocations daily, making us, in essence, already serverless.

But FaaS does come with its challenges. Not all workloads fit the event-based single-operation triggering model, and not all code can be cleanly separated from its dependencies. Some dependencies may require complex installations and configurations, making the migration of existing applications to a FaaS model a significant challenge. Moreover, certain tooling issues have made FaaS products cumbersome to use in certain scenarios, with the best fit being in a microservices architecture context.
<hr>

#### What Is Not Serverless?
One key distinction between PaaS and Serverless lies in the automatic scaling feature. Traditional PaaS providers, like OpenShift and Heroku, do not offer this feature. When using PaaS, you must predefine the necessary resources for your application, and manually scaling up or down becomes your responsibility. Secondly, traditional PaaS is designed for long-running server applications that are continuously active to serve incoming requests. With serverless, your function serves a request and terminates as soon as it's processed. Ideally, your functions shouldn't consume resources when there are no incoming requests.

#### How Are Containers Different?
The rise of Docker marked the arrival of container technology, a lightweight alternative to VMs. Containers package applications to run on a container host, which is, essentially, another server. While containers are a valuable tool, they require hands-on management, which contradicts one of the key principles of serverless: enabling developers to focus on code rather than infrastructure. For containers to become truly serverless, they would need to adopt invocation-based billing based on detailed resource consumption tracking. Nevertheless, there are similarities between serverless and container technologies.

#### Why Go Serverless?
Agile methods have faced criticism for speeding up development without an equivalent pace in product delivery. Serverless architectures can resolve this issue by decoupling application delivery from the need to manage infrastructure. Cloud computing has allowed you to deploy applications without the burden of hardware management, further reducing low-value work to allocate resources to high-value application functionality.

Serverless computing can lead to significant cost savings. Once you adopt serverless, you stop paying for idle resources, a cost often underestimated. Serverless allows you to pay only for what you use. As more organizations recognize the financial benefits of serverless computing, there will be a surge in interest, experimentation, and adoption.

Serverless architecture simplifies deployments and versioning, offering seamless fallback mechanisms and relieving developers of certain responsibilities.

#### What Are the Drawbacks of Serverless?
- Serverless is less efficient for long-running applications, and using serverless for such tasks can be more expensive compared to dedicated servers or VMs.

- Serverless can add complexity rather than reduce it, requiring proper tooling and ecosystem development to address this issue.

- Vendor lock-in is a concern; applications may become dependent on a specific service provider, limiting flexibility and control.

- Additional overhead for function or microservice calls can be introduced in serverless and microservice architectures, as they do not support local operations.

- Serverless may involve multi-tenancy, which can introduce potential bugs and security issues in shared environments.

- Serverless platforms may have a cold start issue, meaning there's an initial delay in handling the first request for a function, but this can be mitigated by keeping functions active with periodic requests.

- Certain vendors lack built-in tools for local function testing, which may lead to unnecessary costs.

- Logging in functions varies among vendors, leaving it to the user to implement more advanced logging.

---

Serverless architecture is a new way of developing and deploying applications, focusing on code while abstracting infrastructure management. While serverless brings numerous benefits, there are also challenges, particularly for long-running applications. Nevertheless, serverless computing is poised to bring about a significant shift in application paradigms, potentially leading to a post-virtual machine, post-container world, and addressing many existing practices and processes.

---


