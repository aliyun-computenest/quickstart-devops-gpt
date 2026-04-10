<h1>DevOpsGPT Community Edition Service Instance Deployment Documentation</h1>

<h2>Overview</h2>

<p>AI-driven Intelligent Software Development Platform (hereinafter referred to as DevOpsGPT). We combine LLMs (Large Language Models) with DevOps tools, leveraging the capabilities of large language models like Chat-GPT to transform natural language requirements into working software. This innovative feature can significantly improve development efficiency, shorten development cycles, and reduce communication costs, thereby delivering higher quality software.</p>

<h2>Billing Description</h2>

<p>The costs for DevOpsGPT Community Edition on Compute Nest mainly involve:</p>
<ul>
    <li>Selected vCPU and memory specifications</li>
    <li>Disk capacity</li>
    <li>Public network bandwidth</li>
</ul>

<p>Billing methods include:</p>
<ul>
    <li>Pay-As-You-Go (hourly)</li>
    <li>Subscription (Yearly/Monthly)</li>
</ul>

<p>Estimated costs can be viewed in real-time during instance creation.</p>

<h2>Required Permissions for RAM Accounts</h2>

<p>The DevOpsGPT service requires access and creation operations for resources such as ECS and VPC. If you use a RAM user to create a service instance, you must add the corresponding resource permissions to the RAM user account before creating the instance. For detailed operations on adding RAM permissions, please refer to <a href="https://help.aliyun.com/document_detail/121945.html" target="_blank">Authorize RAM Users</a>. The required permissions are listed in the table below.</p>

<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th>Permission Policy Name</th>
            <th>Remarks</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>AliyunECSFullAccess</td>
            <td>Permission to manage Elastic Compute Service (ECS)</td>
        </tr>
        <tr>
            <td>AliyunVPCFullAccess</td>
            <td>Permission to manage Virtual Private Cloud (VPC)</td>
        </tr>
        <tr>
            <td>AliyunROSFullAccess</td>
            <td>Permission to manage Resource Orchestration Service (ROS)</td>
        </tr>
        <tr>
            <td>AliyunComputeNestUserFullAccess</td>
            <td>User-side permission to manage Compute Nest services</td>
        </tr>
    </tbody>
</table>

<h3>Deployment Steps</h3>

<ol>
    <li>
        <p>Click the deployment link to enter the service instance deployment interface:<br>
        <a href="https://computenest.console.aliyun.com/user/cn-hangzhou/serviceInstanceCreate?ServiceId=service-6aea16d6e78e4a53924e" target="_blank">https://computenest.console.aliyun.com/user/cn-hangzhou/serviceInstanceCreate?ServiceId=service-6aea16d6e78e4a53924e</a></p>
    </li>
    <li>
        <p>Follow the prompts on the interface to fill in the parameters and complete the deployment.<br>
        Refer to the <strong>Deployment Parameter Description</strong> below to complete the parameter filling, and click <strong>Next: Confirm Order</strong>.</p>
    </li>
    <li>
        <p>Confirm the service instance parameters and estimated price. Check "I have read and agree to the Compute Nest Agreement", then click <strong>Create Now</strong>.</p>
    </li>
    <li>
        <p>Find the service instance on the Service Instance Management page and click <strong>Details</strong> to enter.</p>
    </li>
    <li>
        <p>Once deployment is complete, click the URL to enter the application.</p>
    </li>
</ol>

<h3>Deployment Parameter Description</h3>

<p>During the process of creating a service instance, you need to configure the service instance information. The following details the input parameters for the DevOpsGPT Community Edition service instance.</p>

<table border="1" cellspacing="0" cellpadding="5">
    <thead>
        <tr>
            <th>Parameter Group</th>
            <th>Parameter Item</th>
            <th>Example</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan="1">Service Instance Name</td>
            <td></td>
            <td>test</td>
            <td>Name of the instance</td>
        </tr>
        <tr>
            <td rowspan="1">Region</td>
            <td></td>
            <td>China (Hangzhou)</td>
            <td>Select the region for the service instance. It is recommended to select the nearest region to obtain better network latency.</td>
        </tr>
        <tr>
            <td rowspan="1">Billing Configuration</td>
            <td>Billing Method</td>
            <td>Pay-As-You-Go or Subscription</td>
            <td></td>
        </tr>
        <tr>
            <td rowspan="1">ECS Instance Specification Configuration</td>
            <td>Instance Type</td>
            <td>ecs.g7a.large</td>
            <td>ECS instance specification</td>
        </tr>
        <tr>
            <td rowspan="1">ECS Instance Login Information</td>
            <td>Instance Password</td>
            <td>xxxx</td>
            <td>Set the instance password. Length: 8-30 characters. Must contain at least three of the following: uppercase letters, lowercase letters, digits, and special symbols ()`~!@#$%^&*-+={}[]:;'<>,.?/</td>
        </tr>
        <tr>
            <td rowspan="1">Availability Zone Configuration</td>
            <td>Availability Zone</td>
            <td>Zone I</td>
            <td>Availability zone selection. The choice of availability zone affects VSwitches, instance specifications, etc.</td>
        </tr>
        <tr>
            <td rowspan="5">VPC Configuration</td>
            <td>Create New VPC?</td>
            <td>true</td>
            <td>Whether to create a new VPC.</td>
        </tr>
        <tr>
            <td>VPC Instance ID</td>
            <td>vpc-xxx</td>
            <td>If "Create New VPC" is false, select an existing VPC.</td>
        </tr>
        <tr>
            <td>VSwitch ID</td>
            <td>vsw-xxx</td>
            <td>If "Create New VPC" is false, select an existing VSwitch.</td>
        </tr>
        <tr>
            <td>VPC IPv4 CIDR Block</td>
            <td>192.168.0.0/16</td>
            <td>If "Create New VPC" is true, set the VPC CIDR block.</td>
        </tr>
        <tr>
            <td>VSwitch Subnet CIDR Block</td>
            <td>192.168.1.0/24</td>
            <td>If "Create New VPC" is true, set the VSwitch subnet CIDR block.</td>
        </tr>
        <tr>
            <td rowspan="1">OPENAI Configuration</td>
            <td>OPENAI Key</td>
            <td>sk-xxxx</td>
            <td>API key for underlying OpenAI API calls.</td>
        </tr>
        <tr>
            <td rowspan="4">Github Configuration</td>
            <td>Link GitHub?</td>
            <td>true</td>
            <td>Enable pulling and pushing code from/to GitHub user repositories.</td>
        </tr>
        <tr>
            <td>GitHub Username</td>
            <td>xiaoming</td>
            <td>GitHub username.</td>
        </tr>
        <tr>
            <td>GitHub Email</td>
            <td>xxx@163.com</td>
            <td>GitHub email address.</td>
        </tr>
        <tr>
            <td>GitHub Token</td>
            <td>ghp_xxx</td>
            <td>Configure your Git token. You can obtain it here: <a href="https://github.com/settings/tokens" target="_blank">https://github.com/settings/tokens</a></td>
        </tr>
    </tbody>
</table>

<p>For detailed parameter information, please refer to:<br>
<a href="https://github.com/kuafuai/DevOpsGPT/blob/master/docs/DOCUMENT_CN.md" target="_blank">https://github.com/kuafuai/DevOpsGPT/blob/master/docs/DOCUMENT_CN.md</a></p>

<h3>Verification Results & Usage Demo</h3>

<ol>
    <li>
        <p>Open the URL as per the last step of the deployment steps.</p>
    </li>
    <li>
        <p>Click <strong>APP List</strong> to complete the configuration of custom applications. This mainly includes basic application information, code repository address, development branch, CI/CD configuration, etc. For trial purposes, you can also directly use the sample application.</p>
    </li>
    <li>
        <p>Click <strong>Start task</strong> (Development Requirement, select custom/demo application).</p>
    </li>
    <li>
        <p>Enter the development requirements and start using the product based on the page interaction.</p>
    </li>
    <li>
        <p>After interaction, interface documentation and code will be generated. You can edit and modify them on the page. Clicking <strong>Submit Code</strong> will push the code to the GitHub repository. The code repository address is determined by the <strong>Github Configuration</strong> in the service instance and <strong>APPS.service.git_path</strong> in the application configuration. Please refer to <a href="https://github.com/kuafuai/DevOpsGPT/blob/master/docs/DOCUMENT_CN.md" target="_blank">https://github.com/kuafuai/DevOpsGPT/blob/master/docs/DOCUMENT_CN.md</a></p>
    </li>
    <li>
        <p>For Continuous Integration and Code Deployment, users need to log in to the machine, modify configuration files such as <code>env.yaml</code> in the <code>/root/DevOpsGPT</code> directory according to the reference documentation, and re-execute <code>sh run.sh</code> to take effect.</p>
    </li>
</ol>

<p>Reference Documentation: <a href="https://github.com/kuafuai/DevOpsGPT/blob/master/docs/DOCUMENT_CN.md" target="_blank">https://github.com/kuafuai/DevOpsGPT/blob/master/docs/DOCUMENT_CN.md</a></p>
