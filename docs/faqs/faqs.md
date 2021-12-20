# AWS Virtual Application Management FAQs

## General

Q: What is AWS Virtual Application Management?

Amazon AppStream 2.0 is a fully managed non-persistent application and desktop streaming service that provides users instant access to their desktop applications from anywhere. Amazon AppStream 2.0 simplifies application management, improves security, and reduces costs by moving a company’s applications from their users’ physical devices to the AWS Cloud. The Amazon AppStream 2.0 streaming protocol provides users a responsive, fluid performance that is almost indistinguishable from a natively installed application. With Amazon AppStream 2.0, organizations can realize increased flexibility, improved scalability, and the agility to support a broad range of compute and storage requirements for their applications.

Q: What's the difference between the original Amazon AppStream and Amazon AppStream 2.0?

Amazon AppStream 2.0 is the next-generation desktop application streaming service from AWS. Amazon AppStream was an SDK-based service that customers could use to set up their own streaming service with DIY engineering. AppStream 2.0 provides a fully managed streaming service with no DIY effort. AppStream 2.0 offers a greater range of instance types; streams desktop applications to HTML5-compatible web browsers with no plugins required; provides dual-monitor support on web browsers and 4-monitor, 4K monitor, and USB peripheral support through the AppStream 2.0 client for Windows. In addition, AppStream 2.0 simplifies application lifecycle management and lets your applications access services in your VPC.

Q: Can I continue to use the original Amazon AppStream service?

No. You cannot use the original Amazon AppStream service. Amazon AppStream 2.0 offers a greater range of instance types, streams desktop applications with no rewrite, simplifies application lifecycle management, and allows your apps to access services in your VPC.

Q: What are the benefits of streaming over rendering content locally?

Interactively streaming your application from the cloud provides several benefits:

Instant-on: Streaming your application with Amazon AppStream 2.0 lets your users start using your application immediately, when using an image builder or Always-On fleet, without the delays associated with large file downloads and time-consuming installations.

Remove device constraints: You can leverage the compute power of AWS to deliver experiences that wouldn’t normally be possible due to the GPU, CPU, memory, or physical storage constraints of local devices.

Multi-platform support: You can take your existing applications and start streaming them to a computer without any modifications.

Easy updates: Because your application is centrally managed by Amazon AppStream 2.0, updating your application is as simple as providing a new version of your application to Amazon AppStream 2.0. That's all you need to do to immediately upgrade all your users, without any action on their part.

Improved security: Amazon AppStream 2.0 runs your applications on instances within AWS and only transmits encrypted pixels to end user device. You can apply various security controls provided by AWS to secure your streaming instances. For more details, see Security in Amazon AppStream 2.0.

Q: Do some applications work better with Amazon AppStream 2.0 than others?

Many types of applications work well as streaming applications, including CAD, CAM, CAE, 3D modeling, simulation, games, video and photo-editing software, medical imaging, and life sciences applications. These applications benefit most from streaming because the application runs on the vast computational resources of AWS, yet your users can interact with the application using low-powered devices, with very little noticeable change in application performance.

Q: Does Amazon AppStream 2.0 support microphones?

Yes. Amazon AppStream 2.0 supports most analog and USB microphones, including built-in microphones.

Q: Does Amazon AppStream 2.0 support USB devices such as 3D mice?

Yes. Amazon AppStream 2.0 supports most USB devices such as 3D mice through the Windows Client. All USB devices are disabled by default. Administrators can enable USB devices for their users. 

Q: How do users enable audio input in an Amazon AppStream 2.0 streaming session?

Users enable audio input from the Amazon AppStream 2.0 toolbar by selecting the Settings icon and selecting Enable Microphone.

Q: How can end users use their webcam from within an AppStream 2.0 session?
The Video and Audio Conferencing topic in the AppStream 2.0 documentation provides guidance to help your users use their webcams within an AppStream 2.0 streaming session.

Q: What webcam video resolution does AppStream 2.0 support for streaming sessions?
For streaming sessions, AppStream 2.0 supports a maximum webcam video resolution of 1080p, which measures 1920x1080 pixels.

Q: Can users use their webcam and microphone in an AppStream 2.0 streaming session?
Yes, to learn more visit Real-Time Audio-Video in the AppStream 2.0 documentation. 

Q: How do users manage their webcam video input and microphone audio input during an AppStream 2.0 streaming session?
Users who are connected to a streaming session through the AppStream 2.0 client or a web browser can enable, disable, and select the webcam and microphone to use in their session from the AppStream 2.0 toolbar. 

Q: What is the best AppStream 2.0 instance type to use for streaming video conferencing applications?
The best AppStream 2.0 instance type depends on your video conferencing applications, performance requirements, and environment. We recommend that you test different instance types and evaluate how they perform in your environment with the video conferencing applications that you want to use. Doing so will help you choose the instance type that best suits your needs. For more information about available instance types, see Amazon AppStream 2.0 pricing.

Q: What browsers support real-time audio-video (AV) in an Amazon AppStream 2.0 session?
Google Chrome, Microsoft Edge, Firefox, and additional web browsers support audio-input in Amazon AppStream 2.0 streaming sessions. Microsoft Internet Explorer 11 (IE11) does not support audio-input, and the microphone option will not appear on the Amazon AppStream 2.0 toolbar in streaming sessions running in IE11. To use a local webcam within an AppStream 2.0 streaming session, connect from a Chromium-based web browser, including Google Chrome or Microsoft Edge. 

Q: What does a user need to access applications streamed from Amazon AppStream 2.0?
A user needs to have applications set up by an administrator, a modern web browser that can support HTML5, a broadband internet connection with at least 2 Mbps capability, and outbound access to the internet via HTTPS (443). For web-based AppStream 2.0 streaming sessions, up to two monitors are supported. To use up to four monitors, 4K monitors and USB peripherals such as 3D mice, users can download and use the AppStream 2.0 client for Windows.

Q: What is the AppStream 2.0 Windows Client?

The AppStream 2.0 client for Windows is a native application that is designed for users who require additional functionality not available from web browsers during their AppStream 2.0 streaming sessions. The AppStream 2.0 client lets users use multiple monitors and USB peripherals such as 3D mice with their applications. The client also supports keyboard shortcuts, such as Alt + Tab, clipboard shortcuts, and function keys. The AppStream 2.0 client is supported on the following versions of Windows: Windows 7, Windows 8, Windows 8.1, and Windows 10. Both 32-bit and 64-bit versions of Windows are supported.

Q: What are the system requirements for using the AppStream 2.0 Windows Client?

The minimum system requirements are 2 GB of ram and 150 MB of disk space.

Q: What monitor configurations are supported by the AppStream 2.0 Windows Client?

For browser-based streaming sessions, AppStream 2.0 supports the use of up to two monitors with a maximum display resolution of 2560x1440 pixels per monitor. The AppStream 2.0 client for Windows supports up to 4 monitors with a maximum display resolution of 2560x1440 pixels per monitor. For streaming sessions that are supported by the Graphics Design and Graphics Pro instance families, the AppStream 2.0 client also supports the use of up to 2 monitors with a maximum display resolution of 4096x2160 pixels per monitor.

Q: How can I deploy the AppStream 2.0 Windows Client to my users?

Users can download and install the Windows Client. To use USB peripherials, a users need local administrator rights to install the AppStream 2.0 USB driver. You can remotely install the Windows Client using remote deployment tools like Microsoft System Center Configuration Manager (SCCM). Learn more in our documentation. 

Q: Can users configure location and language settings for their applications?

Yes. Users can set the time zone, locale, and input method to be used in their streaming sessions to match their location and language preferences.

Q: Can users copy and paste between their local device and their Amazon AppStream 2.0 streaming applications?

Yes. Users can use the Windows Client and Google Chrome to access their streaming applications can copy and paste text between their local device and their streaming applications in the same way they copy and paste between applications on their local device - for example, using keyboard shortcuts. For other browsers, users can use the Amazon AppStream 2.0 web clipboard tool.

Q: Can I provide my users a desktop experience?

Yes. AppStream 2.0 allows you to choose between an application or desktop stream view when you configure the fleet. The application view displays only the windows of the applications that are opened by users, while the desktop view displays the standard desktop experience that is provided by the operating system.

Q: Can my Amazon AppStream 2.0 applications run offline?

No. Amazon AppStream 2.0 requires a sustained internet connection or network route to an AppStream 2.0 streaming VPC endpoint to access your applications.

Q: What does Amazon AppStream 2.0 manage on my behalf?

Streaming resources: AppStream 2.0 launches and manages AWS resources to host your application, deploys your application on those resources, and scales your application to meet end user demand.

Simplified app management: Amazon AppStream 2.0 delivers the latest version of an application instantly to users, and eliminates the pain of patching and updating applications on every end-user device. Because your application is centrally managed by AppStream 2.0, updating your application is as simple as providing a new version of your application to AppStream 2.0. Applications can be assigned to users dynamically and removed instantly at any time, improving business flexibility and reducing costs.

Q: Can I use tags to categorize AppStream 2.0 resources?

Yes. you can assign tags to manage and track the following Amazon AppStream 2.0 resources: Applications, appblocks, image builders, images, fleets, and stacks. AWS enables you to assign metadata to your AWS resources in the form of tags. Tags let you categorize your AppStream 2.0 resources so you can easily identify their purpose and track costs accordingly. For example, you can use tags to identify all resources used by a particular department, project, application, vendor, or use case. Then, you can use AWS Cost Explorer to identify trends, pinpoint cost drivers, and detect anomalies in your account.

You can assign or remove tags using the AppStream 2.0 management console, command line interface, or API. Tags have a key and a corresponding value, and you can assign up to 50 tags per AppStream 2.0 resource.

Q. What resources can I create with AWS CloudFormation?

With CloudFormation, you can automate creating fleets, deploying stacks, adding and managing user pool users, launching image builders, and creating directory configurations alongside your other AWS resources.

Q: How do I use my AWS Direct Connect, AWS VPN, or other VPN tunnel to stream my applications?

First, create an Amazon Virtual Private Cloud (Amazon VPC) endpoint in the same Amazon VPC as your AWS Direct Connect, AWS VPN, or other VPN tunnel. Then, specify the VPC endpoint when creating a new stack, modifying an existing one, or creating a new image builder. Your users will then use the VPC endpoint when they stream their applications. To learn more about the AppStream 2.0 streaming VPC endpoints, see Creating and Streaming From VPC Interface Endpoints in the AppStream 2.0 Administration Guide. 
 
## Try sample applications

Q: Can I try sample applications?

Yes. Visit Try Sample Applications low-friction, setup-free trial experience for Amazon AppStream 2.0 service.

Q: What do I need to start using Try It Now?

You need an AWS account and a broadband Internet connection with at least 1 Mbps bandwidth to use Try It Now. You also need a browser capable of supporting HTML5.

Q: Will I be charged for using Try It Now?

You won’t be charged any AWS fees for using Try It Now. However, you may incur other fees such as Internet or broadband charges to connect to the Try It Now experience.

Q: What applications can I use with Try It Now?

Try It Now includes popular productivity, design, engineering, and software development applications running on Amazon AppStream 2.0 for you to try. To see the full list of available applications, go to the Try It Now catalog page after signing in with your AWS account.

Q: How long can I stream applications via Try It Now?

You can stream the applications included in Try It Now for up to 30 minutes. At the end of 30 minutes, your streaming session is automatically terminated and any unsaved data will be deleted.

Q: Can I save files within Try It Now?

You can save files to your Amazon AppStream 2.0 session storage and download them to your client device before your streaming session ends. Your files are not saved when you disconnect from your Try It Now session, or when your session ends, and any unsaved data will be deleted.

Q: Can I submit an application to be included in Try It Now?

Yes. You can submit a request to include your application in Try It Now. After your request is received, AWS usually reviews the request and responds within 10 business days.

## Getting started

Q: How do I get started with Amazon AppStream 2.0?

You can begin using Amazon AppStream 2.0 by visiting the AWS Management Console, or by using the AWS SDK. Visit Stream Desktop Applications for a 10 step tutorial.

Q: What resources do I need to set up to stream my applications using Amazon AppStream 2.0?

You need to create an Amazon AppStream 2.0 stack in your AWS account to start streaming applications to your users. A stack includes a fleet of Amazon AppStream 2.0 instances that executes and streams applications to end users. When you use Elastic fleets, each instance is launched using an AppStream 2.0-managed image, while Always-On and On-Demand fleets use an image that you create containing your applications. You can select the instance type and size for your fleet depending on what CPU, memory, and graphics your user needs. To learn more about Amazon AppStream 2.0 resources, please visit this page.

Q: How do I import my applications to Amazon AppStream 2.0?

If your applications require Active Directory, a custom driver, or require a reboot to install, you will need to create an AppStream 2.0 image using an image builder via the AWS Management Console, then use an Always-On or On-Demand fleet to stream the applications to your users. Image Builder allows you to install and test your applications just as you would with any Microsoft Windows or Linux desktop, and then create an image. You can complete all the install, test, and creation steps for the image without leaving the console.

If your applications don’t require Active Directory and can be run from virtual hard disks without being configured, you can package them within virtual hard disks and upload them to an S3 bucket within your account. Once you have uploaded your applications, you can create AppStream 2.0 app block and application resources, and assign them to an AppStream 2.0 Elastic fleet to stream to your users.

Q: How do I create an Amazon AppStream 2.0 image to import my applications?

You can create an Amazon AppStream 2.0 image using Image Builder via the AWS Management Console. Image Builder allows you to install and test your applications just as you would with any Windows or Linux desktop, and then create an image. You can complete all the install, test, and creation steps for the image without leaving the console.

Q: What instance types are available to use with my Amazon AppStream 2.0 fleet?

Amazon AppStream 2.0 provides a menu of instance types for configuring a fleet or an image builder. You can select the instance type that best matches your applications and end-user requirements. You can choose from General Purpose, Compute Optimized, Memory Optimized, Graphics Design, Graphics Pro and Graphics G4 instance families. 

Q: Can I change an instance type after creating a fleet?

Yes. You can change your instance type after you have created a fleet. To change the instance type, you will need to stop the fleet, edit the instance type, and then start the fleet again. For more information, see Set up AppStream 2.0 Stacks and Fleets.

Q: Can I connect Amazon AppStream 2.0 instances to my VPC?

Yes. You can choose the VPCs to which your Amazon AppStream 2.0 instances (fleet and image builders) connect. When you create your fleet, or launch Image Builder, you can specify one or more subnets in your VPC. If you have a VPC with a VPN connection to your on-premises network, then Amazon AppStream 2.0 instances in your fleet can communicate with your on-premises network. You retain the usual control you have over network access within your VPC, using all the normal configuration options such as security groups, network access control lists, and routing tables. For more information about creating a VPC and working with subnets, see Working with VPCs and Subnets.

Q: Can I use custom branding with Amazon AppStream 2.0?

Yes. You can customize your users' Amazon AppStream 2.0 experience with your logo, color, text, and help links in the application catalog page. To replace AppStream 2.0's default branding and help links, log in to the AppStream 2.0 console, navigate to Stacks, and select a your application stack. Then, click Branding, choose Custom, select your options, and click Save. Your custom branding will apply to every new application catalog launched using SAML 2.0 single-sign-on (SSO) or the CreateStreamingURL API. You can revert to the default AppStream 2.0 branding and help links at any time. To learn more, visit Add Your Custom Branding to Amazon AppStream 2.0.

Q: Can I define default application settings for my users?

Yes, you can set default application settings for your users. This includes application connection profiles, browser settings, and installing plugins.

Q: Can users save their application settings?

Yes. You can enable persistent application and Windows settings for your users on AppStream 2.0. Your users' plugins, toolbar settings, browser favorites, application connection profiles, and other settings will be saved and applied each time they start a streaming session. Your users' settings are stored in an S3 bucket you control in your AWS account.

To learn more about persistent application settings, see Enable Application Settings Persistence for Your AppStream 2.0 Users.

Q: Am I charged for persistent user application settings?

There is no additional AppStream 2.0 charge to use this feature. However, persistent user application settings are stored in an Amazon S3 bucket in your account, and you will be billed for the S3 storage used for your user’s settings data. See Amazon S3 pricing or Enable Application Settings Persistence for Your AppStream 2.0 Users for more information.

Q: Is there a limit to the file size of my users' persistent application settings?
By default, the maximum user profile file size is 1 GB. See Enable Application Settings Persistence for Your AppStream 2.0 Users to increase this.

Q: Will my users' application settings persist across stacks?
Yes. Your users' application settings persist across stacks.

Q: How are my users' application settings secured?
Your users' application settings are encrypted in transit to the S3 bucket in your account using Amazon S3's SSL endpoints. Your users' application settings are encrypted at rest using S3-managed encryption keys.

Q: Can I dynamically entitle users to apps?
Yes, you can use the dynamic app framework APIs to build a dynamic app provider that specifies what apps uers can launch at run-time. The apps provided can be virtualized apps that are delivered from a Windows file share or other storage technology. To learn more, see Manage App Entitlement with the Dynamic App Framework.

## Images

Q: How can I create images with my own applications?

You can use Amazon AppStream 2.0 Image Builder to create images with your own applications. To learn more, please visit the tutorial found on this page.

Q: With which operating system do my apps need to be compatible?

Amazon AppStream 2.0 streams applications that can run on the following 64-bit Windows OS versions - Windows Server 2012 R2, Windows Server 2016 and Windows Server 2019. You can add support for 32-bit Windows applications by using the WoW64 extensions. If your application has other dependencies, such as the .NET framework, include those dependencies in your application installer. Amazon AppStream 2.0 also streams applications that can run on Amazon Linux 2 operating system.

Q: Can I install anti-virus software on my Amazon AppStream 2.0 image to secure my applications?

You can install any tools, including anti-virus programs on your AppStream 2.0 image. However, you need to ensure that these applications do not block access to the AppStream 2.0 service. We recommend testing your applications before publishing them to your users. You can learn more by reading Windows Update and Antivirus Software on AppStream 2.0 and Data Protection in AppStream 2.0 in the Amazon AppStream 2.0 Administration Guide.

Q: Can I customize the Windows operating system using group policies?

Any changes that are made to the image using Image Builder through local group policies will be reflected in your AppStream 2.0 images. Any customizations made with domain based group policies can only be applied to domain joined fleets.

Q: How do I keep my Amazon AppStream 2.0 images updated?

AppStream 2.0 regularly releases base images that include operating system updates and AppStream 2.0 agent updates. The AppStream 2.0 agent software runs on your streaming instances and enables your users to stream applications. When you create a new image, the *Always use latest agent version* option is selected by default. When this option is selected, any new image builder or fleet instance that is launched from your image will always use the latest AppStream 2.0 agent version. If you deselect this option, your image will use the agent version you selected when you launched the image builder. Alternatively, you can use managed AppStream 2.0 image updates with your images to install the latest operating system updates, driver updates, and AppStream 2.0 agent software and create new images. You are responsible for installing and maintaining the updates for the operating system, your applications, and their dependencies. For more information, see Keep Your AppStream 2.0 Image Up-to-Date.

Q: How do I update my applications in an existing image?

To update applications on the image, or to add new applications, launch Image Builder using an existing image, update your applications and create a new image. Existing streaming instances will be replaced with instances launched from the new image within 16 hours or immediately after users have disconnected from them, whichever is earlier. You can immediately replace all the instances in the fleet with instances launched from the latest image by stopping the fleet, changing the image used, and starting it again.

Q: Can I connect my Amazon AppStream 2.0 applications to my existing resources, such as a licensing server?

Yes. Amazon AppStream 2.0 allows you to launch streaming instances (fleets and image builders) in your VPC, which means you can control access to your existing resources from your AppStream 2.0 applications. For more information, see Network Settings for Fleet and Image Builder Instances.

Q. Can I copy my Amazon AppStream 2.0 images?

Yes. You can copy your Amazon AppStream 2.0 application images across AWS Regions. To copy an image, launch the AppStream 2.0 console and select the region that contains your existing image. In the navigation pane, choose Images, select your existing image, click Actions, select Copy, and pick your target AWS Region. You can also use the CopyImage API to programmatically copy images. Visit Tag and Copy an Image for more information.

Q: Can I share application images with other AWS Accounts?

Yes. You can share your AppStream 2.0 application images with other AWS accounts within the same AWS Region. You control the shared image and can remove it from another AWS account at any time. To learn more, visit Administer Your Amazon AppStream 2.0 Image

Q: What permissions can I give other AWS accounts when I share my application image(s) with them?

You maintain full privileges to the application image. You can share the image with other AWS accounts, granting them permission to either create image builders, use for fleets, or both. These permissions can later be revoked. However, if you granted the destination AWS account permission to create image builders, you will not be able to revoke access to the image builders or images they create from your image.

Q: If I share an application image with another AWS account, can I delete it or remove permissions?

Yes. You control the image. In order to delete the image, you will first have to stop sharing the image from all AWS accounts you shared it with. The AWS accounts you shared the image with will no longer see the image in their Image Registry, and will be unable to select it for new or existing fleets. Existing streaming instances in the fleets will continue to stream applications, but the fleet will terminate existing unused instances. If you originally granted permissions for creating image builders, they will be unable to create new image builders from it, but existing ones will continue to work. Images in the destination account created from image builders from the shared image will continue to work.

## Graphics instances

Q: Does Amazon AppStream 2.0 offer GPU-accelerated instances?

Yes. Amazon AppStream 2.0 offers Graphics Design, Graphics Pro and Graphics G4 instance families.

Graphics Design instances are ideal for delivering applications such as Adobe Premiere Pro, Autodesk Revit, and Siemens NX that rely on hardware acceleration of DirectX, OpenGL, or OpenCL. Powered by AMD FirePro S7150x2 Server GPUs and equipped with AMD Multiuser GPU technology, instances start from 2 vCPU, 7.5 GiB system memory, and 1 GiB graphics memory, to 16 vCPUs, 61 GiB system memory, and 8 GiB graphics memory.

Graphics g4dn instances are based on the EC2 G4 family. Amazon EC2 g4dn instances deliver the industry’s most cost-effective and versatile GPU instance for running graphics-intensive applications on AWS. G4dn instances provide the latest generation NVIDIA T4 GPUs, AWS custom Intel Cascade Lake CUs, up to 100 Gbps of networking throughput, and up to 1.8 TB of local NVMe storage. These instances are ideal for streaming graphics intensive applications that rely on NVIDIA GPU libraries such as CUDA using AppStream 2.0. AppStream 2.0 offers six different g4dn instance sizes, ranging from 4 vCPUs and 16 GiB of memory to 64 vCPUs and 256 GiB of memory

The Graphics Pro instance family offers three different instance types to support the most demanding graphics applications. Powered by NVIDIA Tesla M60 GPUs with 2048 parallel processing cores, there are three Graphics Pro instances types starting from 16 vCPUs, 122 GiB system memory, and 8 GiB graphics memory, to 64 vCPUs, 488 GiB system memory, and 32 GiB graphics memory. These instance types are ideal for graphic workloads that need a massive amount of parallel processing power for 3D rendering, visualization, and video encoding, including applications such as Petrel from Schlumberger Software, Landmark's DecisionSpace, or MotionDSP's Ikena. For more information on available instance types and pricing, see Amazon AppStream 2.0 pricing.

## Fleets

Q: What are fleets?

Fleets are an AppStream 2.0 resource that represent the configuration details for the streaming instances your users will use to launch their applications and desktops. The fleet consists of configuration details such as instance type and size, networking, and user session timeouts.

Q: What types of fleets are available with Amazon AppStream 2.0?

Amazon AppStream 2.0 offers three fleet types: Always-On, On-Demand, and Elastic. These fleet types allow you to choose how applications and desktops are delivered, the speed of session start, and cost to stream.

Q: What are the differences between the fleet types?

Always-On and On-Demand fleet streaming instances are launched using the custom AppStream 2.0 image that you create that contains your applications and configurations. You can specify how many instances to launch manually, or dynamically using Fleet Auto Scaling policies. Streaming instances must be provisioned before a user can stream.

Elastic fleet streaming instances are launched using an AppStream 2.0 managed image, with applications and configurations delivered at run time. AppStream 2.0 manages the capacity of Elastic fleets for you. Elastic fleets only support applications from App Blocks, and cannot be joined to a Microsoft Active Directory domain.

Q: Can I switch my Amazon AppStream 2.0 Always-On fleet to On-Demand or vice versa?

You can only specify the fleet type when you create a new fleet, and you cannot change the fleet type once the fleet has been created.

Q: What are the benefits to Always-On and On-Demand fleets for Amazon AppStream 2.0?

Always-On and On-Demand fleets are best for when your applications require Microsoft Active Directory domain support, or can only be delivered using an AppStream 2.0 image. Always-On fleet streaming instances provide instant access to applications and you pay the running instance rate even when no users are streaming. On-Demand fleet streaming instances launch the application after an up to 2-minute wait, and you pay the running instance rate only when users are streaming. On-Demand fleet streaming instances that are provisioned but not yet used are charged at a lower stopped instance fee. You manage the capacity of Always-On and On-Demand fleet streaming instances using auto scaling rules.

Elastic fleet streaming instances launch the requested application after it has been downloaded and mounted to the streaming instance, and you only pay the running instance rate for the duration of the user’s streaming session. AWS manages the streaming instance availability, and no auto scaling rules are required.
  	On-Demand 	Always-On 	Elastic
Applications 	Custom image 	Custom image 	App blocks
 Instances 	Stopped 	Running 	Running
Capacity management 	Customer managed with auto scaling 	Customer managed with auto scaling 	AWS managed
User session start 	Up to 2 minutes 	Instant on 	Up to 1 minutes
Use cases 	Use cases where cost savings are critical such as education 	Businesses that need instant availability of applications 	Trials, trainings, and demos, and converting software to software as a service 

## Applications for Elastic Fleets

Q: What applications can I use with an Elastic fleet?

Elastic fleets can use applications that are designed to be self-contained, portable and can operate off a different volume. This is similar to installing an application to a USB hard disk drive, and running it from any PC you use.

Q: How do I import my applications for Elastic fleets?

Elastic fleets use applications that are saved within virtual hard disk (VHD) files and saved to an S3 bucket within your AWS account. The VHD is downloaded to the streaming instance and mounted when your user chooses which application to launch. To learn more about importing applications for Elastic fleets, read Create and Manage App Blocks and Applications for Elastic Fleets in the Amazon AppStream 2.0 Administration Guide.

Q: What are AppStream 2.0 AppBlocks and AppStream 2.0 Applications?

AppBlocks are an AppStream 2.0 resource that has the details for the virtual hard drive with your application’s files, and the setup script for how to mount it to the streaming instance. Applications are an AppStream 2.0 resource that has the details for how to launch applications from an AppBlock. You must associate your Applications to AppBlocks before you can associate them to the Elastic fleet.

Q: How are App Blocks mounted to an Elastic fleet streaming instance?

When you create the App Block, you must specify a setup script. The setup script specifies how to mount the App Block to the streaming instance, and allows you to complete any customization or configuration needed before the application launches. To learn more about creating the setup script, read Create the Setup Script for the VHD in the Amazon AppStream 2.0 Administration Guide
Platform support

Q: What client operating systems and browsers are supported?

Amazon AppStream 2.0 can stream your applications to HTML5-compatible browsers, including the latest versions of Google Chrome, Mozilla Firefox, Microsoft Internet Explorer, and Microsoft Edge, on desktop devices, including Windows, Mac, Chromebooks, and Linux PCs. The AppStream 2.0 client for Windows lets your users use 4 monitors, 4K monitors and and USB peripherals such as 3D mouse with your applications on AppStream 2.0. The AppStream 2.0 client for Windows is supported on the following versions of Windows: Windows 7, Windows 8, Windows 8.1, and Windows 10. Both 32-bit and 64 bit versions of Windows are supported.

Q: What Windows server operating system is supported?

Amazon AppStream 2.0 streams applications that can run on the following 64-bit OS versions - Windows Server 2012 R2, Windows Server 2016 and Windows Server 2019. You can add support for 32-bit applications by using the WoW64 extensions. If your application has other dependencies, such as the .NET framework, include those dependencies in your application installer.

Q: Which Linux distribution is supported?

Amazon AppStream 2.0 supports Amazon Linux 2 operating system.

Q: Which AWS regions does Amazon AppStream 2.0 support?

Please refer to the AWS Regional Products and Services page for details of Amazon AppStream 2.0 service availability by region

Q: What instance types are available to use with my Amazon AppStream 2.0 fleet?

Amazon AppStream 2.0 provides a menu of instance types for configuring a fleet. You can select the instance type that best matches your applications and end-user requirements. You can choose from General Purpose, Compute Optimized, Memory Optimized, Graphics Design, Graphics Desktop, or Graphics Pro instance families.

## Auto scaling

Q: How does Amazon AppStream 2.0 scale?

Amazon AppStream 2.0 Always-On and On-Demand fleets use Fleet Auto Scaling to launch Amazon AppStream 2.0 instances running your application and to adjust the number of streaming instances to match the demand for end-user sessions. Each end-user session runs on a separate instance, and all of the applications that are streamed within a session run on the same instance. An instance is used to stream applications for only one user, and is replaced with a new instance at the end of the session. For more information, read Fleet Auto Scaling for Amazon AppStream 2.0 in the Amazon AppStream 2.0 Administration Guide.

The capacity of Elastic fleets is fully managed for you, and does not require any autoscaling policies.

Q: What scaling policy does Amazon AppStream 2.0 support?

You can set a fixed fleet size to keep a constant number of AppStream 2.0 streaming instances, or use dynamic scaling policies that adjust capacity based on a schedule, usage, or both. Using dynamic scaling policies allows you to manage your cost while ensuring there is sufficient capacity for your users to stream. For more information, read Fleet Auto Scaling for Amazon AppStream 2.0 in the Amazon AppStream 2.0 Administration Guide.

Q: What is an Amazon AppStream 2.0 Fleet Auto Scaling policy?

A Fleet Auto Scaling policy is a dynamic scaling policy that allows you to scale the size of your fleet to match the supply of available instances to user demand. You can define scaling policies that adjust the size of your fleet automatically based on a variety of utilization metrics, and optimize the number of running instances to match user demand. For more information, read Fleet Auto Scaling for Amazon AppStream 2.0 in the Amazon AppStream 2.0 Administration Guide.

Q: How can I create auto scaling policies for my Amazon AppStream 2.0 fleet?

You can create automatic scaling policies from the Fleets tab in the AppStream 2.0 console, or by using the AWS SDK.

Q: Which Amazon AppStream 2.0 CloudWatch metrics can I use to build Fleet Auto Scaling polices?

You can use the following metrics to build your Fleet Auto Scaling policies:

• Capacity utilization: you can scale your fleet based on the percentage of instances in your fleet that are being used
• Available capacity: you can scale your fleet based on the number of available instances in your fleet
• Insufficient capacity error: you can provision new instances when users can’t start streaming sessions due to lack of capacity

For more information, please see Fleet Auto Scaling for Amazon AppStream 2.0.

Q: Can my Amazon AppStream 2.0 fleet have more than one associated Fleet Auto Scaling policy?

Yes. You can have up to 50 Fleet Auto Scaling policies associated with a single fleet. Each policy allows you to set a single criteria and action for resizing your fleet.

Q: What is the minimum size I can set for my Amazon AppStream 2.0 fleet when using Fleet Auto Scaling policies?

You can set your Fleet Auto Scaling policies to scale in to zero instances. Scaling policies associated with your fleet decrease fleet capacity until it reaches your defined minimum, or the default setting of one if you haven’t set a minimum. For more information, please see Fleet Auto Scaling for Amazon AppStream 2.0.

Q: What is the maximum size I can set for my Amazon AppStream 2.0 fleet when using Fleet Auto Scaling policies?

Fleet Auto Scaling policies increase fleet capacity until it reaches your defined maximum size or until service limits apply. For more information, please see Fleet Auto Scaling for Amazon AppStream 2.0. For service limit information, please see Amazon AppStream 2.0 Service Limits.

Q: Are there additional costs for using Fleet Auto Scaling policies with Amazon AppStream 2.0 fleets?

There are no charges for using Fleet Auto Scaling policies. However, each CloudWatch alarm that you create and use to trigger scaling policies for your AppStream 2.0 fleets may incur additional CloudWatch charges. For more information, see Amazon CloudWatch Pricing.

## Persistent storage

Q: Does Amazon AppStream 2.0 offer persistent storage so that I can save and access files between sessions?

Yes. Amazon AppStream 2.0 offers multiple options for persistent file storage to allow users to store and retrieve files between their application streaming sessions. You can use a home folder backed by Amazon S3, Google Drive for G Suite, or Microsoft OneDrive for Business. Each of these are accessed from the my files tab within an active AppStream 2.0 streaming session, and content can be saved or opened directly from the File menu in most apps.

Home folders are AppStream 2.0's native persistent storage option. Users can access a home folder on their streaming instance and save content in their folder. Files are stored in an S3 bucket which is automatically created in your AWS account. To learn more, visit Enable and Administer Home Folders for Your AppStream 2.0 Users.

For Windows OS based AppStream 2.0 stacks, you can enable Google Drive for G Suite, and users can link their G Suite account to access files on Google Drive. Changes are automatically synced with Google Drive. To learn more, visit Enable and Administer Google Drive for Your AppStream 2.0 Users.

For Windows OS based AppStream 2.0 stacks, you can enable Microsoft OneDrive for Business, and users can link their OneDrive for Business account to access their files on OneDrive. Changes are automatically synced with OneDrive for Business. To learn more, visit Enable and Administer OneDrive for Your AppStream 2.0 Users.

Q: How do users access persistent storage from their Amazon AppStream 2.0 sessions?

Users can access a home folder during their application streaming session. Any file they save to their home folder will be available for use in the future. They can also connect their G Suite account to access Google Drive and connect their Microsoft OneDrive for Business account to access OneDrive within AppStream 2.0. New files added or changes made to existing files within a streaming session are automatically synced between AppStream 2.0 and their persistent storage options.

Q. Can I enable multiple persistent storage options for an Amazon AppStream 2.0 stack?

Yes. You can enable Home Folders, Google Drive for G Suite, and Microsoft OneDrive for Business. To optimize your internet bandwidth, create a VPC endpoint for Amazon S3 and authorize AppStream 2.0 to access your VPC endpoint. This routes Home Folders data through your VPC and Google Drive or OneDrive data through the public Internet.

Q. How do I enable Google Drive for G Suite for Amazon AppStream 2.0?

When creating an Amazon AppStream 2.0 stack, select the option to enable Google Drive for the stack, provide your G Suite domain names, and create the stack. To learn more, visit Enable and Administer Google Drive for Your AppStream 2.0 Users.

Q. Can a user remove their Google Drive for G Suite account?

Yes. Users can remove permissions that AppStream 2.0 has to their Google account from their Google account permissions page.

Q. Can I control which Google Drive for G Suite accounts integrate with AppStream 2.0?

Yes. Only user accounts with your G Suite organization's domain name can use their Google Drive account. Users cannot link any other accounts. To learn more, visit Enable and Administer Google Drive for Your Users.

Q. What kind of data can users store in Google Drive during a streaming session?

Any file type that is supported by Google Drive can be stored during the streaming session. For more details on the file types supported by Google Drive, refer to Google Drive FAQs.

Q. Can users transfer files from their device to Google Drive during their streaming session?

Yes. Users can transfer files to and from from their device and Google Drive using the MyFiles feature in the streaming session toolbar. Visit Enable Persistent Storage for Your AppStream 2.0 Users to learn more.

Q. How do I enable Microsoft OneDrive for Business for Amazon AppStream 2.0?

When creating an Amazon AppStream 2.0 stack, select the option to enable OneDrive for Business for the stack, provide your OneDrive for Business domain names, and create the stack. To learn more, visit Enable and Administer OneDrive for Your AppStream 2.0 Users.

Q. Can I control which Microsoft OneDrive for Business accounts integrate with AppStream 2.0?

Yes. Only user accounts with your OneDrive for Business domain names can use their accounts. Users cannot link any other accounts. To learn more, visit Enable and Administer OneDrive for Your AppStream 2.0 Users.

Q. Can a user remove Microsoft OneDrive for Business?

Yes. Users can remove permissions that AppStream 2.0 has to their OneDrive for Business online account.

Q. What kind of data can users store in Microsoft OneDrive for Business during a streaming session?

Any file type that is supported by OneDrive for Business can be stored during the streaming session. For more details on the file types supported by OneDrive for Business, refer to OneDrive for Business documentation.

Q. Can users transfer files from their device to Microsoft OneDrive for Business during their streaming session?

Yes. Users can transfer files to and from from their device and OneDrive for Business using the MyFiles feature in the streaming session toolbar. To learn more, visit Enable and Administer OneDrive for Your AppStream 2.0 Users.

## Monitoring

Q: How do I monitor usage of my Amazon AppStream 2.0 fleet resources?

There are two ways you can monitor your Amazon AppStream 2.0 fleet. First, the AppStream 2.0 console provides a lightweight, real-time view of the state of your AppStream 2.0 fleet, and offers up to two weeks of historical usage data. Metrics are displayed automatically, and don’t require any setup.

Second, you can access AppStream 2.0 metrics using CloudWatch. The CloudWatch console allows you to specify reporting intervals, create custom dashboards and graphs, and set alarms.

To learn more, see Monitoring Amazon AppStream 2.0 Resources.

Q: What information can I get from the Amazon AppStream 2.0 usage metrics?

You can see the size of your Amazon AppStream 2.0 fleet, the number of running instances, the number of instances available to accept new connections, and the utilization of your fleet. You can track these metrics over time so that you can optimize your fleet settings to suit your needs.

Using Amazon CloudWatch, you can also set alarms to notify you of changes to your fleet, or when there is insufficient capacity to support your users.

For the complete list of available metrics, see Monitoring Amazon AppStream 2.0 Resources.

Q: Can I create custom Amazon CloudWatch metrics for Amazon AppStream 2.0?

Yes, you can create custom metrics for Amazon AppStream 2.0. For more information, see Publish Custom Metrics.

Q: How frequently are Amazon AppStream 2.0 metrics published to Amazon CloudWatch?

Amazon AppStream 2.0 sends metrics to Amazon CloudWatch every 1 minute. The metrics are stored in CloudWatch using the standard retention policy. For more information, see Amazon CloudWatch FAQs.

Q: How do I create CloudWatch alarms for Amazon AppStream 2.0?

You can create Amazon CloudWatch alarms for Amazon AppStream 2.0 using the CloudWatch console or the CloudWatch APIs.

Q: Are there additional costs for using CloudWatch metrics with Amazon AppStream 2.0?

There is no additional charge for viewing CloudWatch metrics for AppStream 2.0. You may incur additional charges for setting up CloudWatch alarms and retrieving metrics via the CloudWatch APIs. For more information, see Amazon CloudWatch Pricing.

Q: Does Amazon AppStream 2.0 offer a set of public APIs?

Yes, Amazon AppStream 2.0 includes APIs that you can use to easily integrate and extend the service. The APIs enable you to create, update, and delete Amazon AppStream 2.0 resources, and provide detailed information about resource states. You can create URLs for administrators to connect to their image builders to install applications, and create URLs for users to access their AppStream 2.0 applications. See our API reference for more information.

## Streaming

Q: What streaming protocol does Amazon AppStream 2.0 use?

Amazon AppStream 2.0 uses NICE DCV to stream your applications to your users. NICE DCV is a proprietary protocol used to stream high-quality, application video over varying network conditions. It streams video and audio encoded using standard H.264 over HTTPS. The protocol also captures user input and sends it over HTTPS back to the applications being streamed from the cloud. Network conditions are constantly measured during this process and information is sent back to the encoder on the server. The server dynamically responds by altering the video and audio encoding in real time to produce a high-quality stream for a wide variety of applications and network conditions.

Q: What is the maximum network latency recommended while accessing Amazon AppStream 2.0?

While the remoting protocol has a maximum round-trip latency recommendation of 250 ms, the best user experience is achieved at less than 100 ms. If you are located more than 2000 miles from the AWS Regions where Amazon AppStream 2.0 is currently available, you can still use the service, but your experience may be less responsive.
Security

Q: How do I restrict network access from fleets and image builders launched in my VPC?

Security groups enable you to specify network traffic that is allowed between your streaming instances and resources in your VPC. You can restrict network access by assigning an image builder or fleet to the security groups in your VPC. For more information, refer to Security Group for Your VPC.

Q: Can I use existing VPC security groups to secure AppStream 2.0 fleets and image builders?

Yes. You can assign an image builder or fleet to existing security groups in your VPC.

Q: How many security groups can I apply to a fleet or image builder?

You can assign an image builder or fleet to up to five security groups.

Q: Can I change the security groups to which my fleets are assigned after they have been created?

Yes. You can change the security groups to which your fleets are assigned, so long as they are in the stopped status.

You can also change the rules of a security group in your VPC at any time using the Amazon EC2 console. Note that the new rules will apply to all resources assigned to that security group. For more information, refer to Security Groups for your VPC.

Q: Can I change the security groups to which my image builders are assigned after they have been created?

No. You cannot change the security groups to which your fleets are assigned after they have been created. To assign an image builder to a different security groups, you will need to create a new image builder.

You can also change the rules of a security group in your VPC at any time using the Amazon EC2 console. Note that the new rules will apply to all resources assigned to that security group. For more information, refer to Security Groups for your VPC.

Q: How is the data stored in my user's home folders secured?

Files and folders in your users' home folders are encrypted in transit using Amazon S3's SSL endpoints. Files and folders are encrypted at rest using Amazon S3-managed encryption keys.

Q: How is the data from my streamed application encrypted to the client?

The streamed video and user inputs are sent over HTTPS and are SSL-encrypted between the Amazon AppStream 2.0 instance executing your applications, and your end users.

Q. Can I control data transfer between AppStream 2.0 and my users' devices?

Yes. You can choose whether to allow users to transfer data between their streaming applications and their local device through copy or paste, file upload or download, or print actions. To learn move, visit Create Fleets and Stacks.

## Identity

Q: How do I authenticate users with Amazon AppStream 2.0 applications?

There are three options to authenticate users with Amazon AppStream 2.0: you can use built-in user management, you can build a custom identity, or you can set up federated access using SAML 2.0.

When using built-in user management, you can set up and manage your users in the AppStream 2.0 management console from the User Pool tab. To add a new user, all you need is their first and last name, and an e-mail address. To learn more about user management within AppStream 2.0, see Using the AppStream 2.0 User Pool.

When using federated sign-in to authenticate users, you will set up identity federation using SAML 2.0, which allows you to use your existing user directory to control access to applications available via AppStream 2.0. For details on setting up SAML integration, see the steps outlined here.

When building an entitlement service, you should authenticate users either with a custom identity or by using a service such as Login with Amazon. After your custom identity has authenticated a user, it should call into Amazon AppStream 2.0 to create a new streaming URL. AppStream 2.0 returns a URL for the session that can be opened in a browser to start the streaming session.

Q: Can I use Amazon AppStream 2.0 with my existing user directory, including Microsoft Active Directory?

Yes. Amazon AppStream 2.0 supports identity federation using SAML 2.0, which allows you to use your existing user directory to manage end user access to your AppStream 2.0 apps. For details on setting up SAML integration, read Single Sign-on Access (SAML 2.0) in the Amazon AppStream 2.0 Administration Guide.

Q: What type of identity federation does Amazon AppStream 2.0 support?

Amazon AppStream 2.0 supports federation using SAML 2.0 (Identity Provider initiated). This type of federated access allows a user to sign in by first authenticating with an identity federation provider, after which they can access their AppStream 2.0 apps.

Q: What are the requirements for setting up identity federation with Amazon AppStream 2.0?

To configure identity federation with Amazon AppStream 2.0, you need a SAML 2.0 Identity Provider that links to an existing LDAP-compatible directory, such as Microsoft Active Directory. Microsoft Active Directory Federation Services (ADFS), Ping Identity, Okta, and Shibboleth, are all examples of SAML 2.0 Identity Providers that will work with AppStream 2.0.

Q: Can I control which users access my Amazon AppStream 2.0?

Yes. When using built-in user management, you can control which users have access to your Amazon AppStream 2.0 stacks in the User Pool tab of the AppStream 2.0 management console. To learn more about user management within AppStream 2.0, see Using the AppStream 2.0 User Pool.

When you use SAML 2.0, you can control which users have access to your Amazon AppStream 2.0 stacks by mapping the users in your federation service to the IAM role that has access permissions to the stack. Please refer to the AppStream 2.0 documentation for detailed information and step-by-step guidelines for popular federation services.

Q: Can I enable multi-factor authentication for my users?

Yes. You can enable Multi-Factor Authentication when using federation with SAML 2.0 or when using your own entitlement service.

Q: Can users choose which Amazon AppStream 2.0 stack they want to access during signing-in?

Yes. You can setup every Amazon AppStream 2.0 stack as an entity or a package in your federation service. This allows your users to select which stack they want to access while signing in from your application portal.

Q: Who can access the management console for my Amazon AppStream 2.0 application?

You can use AWS Identity and Access Management (IAM) to add users to your AWS account and grant them access to view and manage your Amazon AppStream 2.0 application. For more information, see “What is IAM?” in the IAM User Guide.

## Microsoft Active Directory domain support

Q: Can I join Amazon AppStream 2.0 image builders to Microsoft Active Directory domains?

Yes, Amazon AppStream 2.0 Windows OS-based streaming instances can be joined to your Microsoft Active Directory domains. This allows you to apply your existing Active Directory policies to your streaming instances, and provides your users with single sign on access to Intranet sites, file shares, and network printers from within their applications. Your users are authenticated using a SAML 2.0 provider of your choice, and can access applications that require a connection to your Active Directory domain. You can join image builders, Always-On fleet streaming instances, and On-Demand fleet streaming instances that use the Windows OS to Active Directory domains. Linux OS-based AppStream 2.0 image builders, Always-On fleet streaming instances, and On-Demand fleet streaming instances cannot be joined to Active Directory domains.

Q: What Microsoft Active Directory versions are supported?

Microsoft Active Directory Domain Functional Level Windows Server 2008 R2 and newer are supported by Amazon AppStream 2.0.

Q: Which AWS Directory Services directory options are supported by Amazon AppStream 2.0?

Amazon AppStream 2.0 supports AWS Directory Services Microsoft AD. Other options such as AD Connector and Simple AD are not supported. To learn more about AWS Microsoft AD see What Is AWS Directory Service.

Q: How do I join my Amazon AppStream 2.0 instances to my Microsoft Active Directory domain?

To get started you will need a Microsoft Active Directory domain that is accessible from an Amazon VPC, the credentials of a user with authority to join the domain, and the domain Organizational Unit (OU) you want to join to your fleet. For more information, see Using Active Directory Domains with AppStream 2.0.

Q: Can I use my existing Organization Units (OU) structure with Amazon AppStream 2.0?

Yes, you can use your existing Organizational Unit (OU) structure with Amazon AppStream 2.0. To learn more, see Using Active Directory Domains with AppStream 2.0.

Q: What gets joined to my Microsoft Active Directory domain by Amazon AppStream 2.0?

Amazon AppStream 2.0 will automatically create a unique computer object for every image builder and Always-On or On-Demand fleet instance you configure to be joined to your Microsoft Active Directory domain.

Q: How can I identify Amazon AppStream 2.0 computer objects in my Microsoft Active Directory domain?

Amazon AppStream 2.0 computer objects are only be created in the Microsoft Active Directory Organization Unit (OU) you specify. The description field indicates that the object is an AppStream 2.0 instance, and to which fleet the object belongs. To learn more, see Using Active Directory Domains with AppStream 2.0.

Q: How are computer objects that are created by Amazon AppStream 2.0 deleted from my Microsoft Active Directory domain?

Computer objects created by Amazon AppStream 2.0 that are no longer used will remain in your Active Directory (AD) if the AppStream 2.0 fleet or image builder is deleted, you update a fleet or image builder to a new OU, or select a different AD. To remove unused objects you will have to delete them manually from your AD domain. To learn more, see Using Active Directory Domains with AppStream 2.0.

Q: How do I provide users with access to Amazon AppStream 2.0 streaming instances that are joined to a Microsoft Active Directory domain?

To enable user access, you will need to set up federated access using a SAML 2.0 provider of your choice. This allows you to use your existing user directory to control access to streaming applications available via Amazon AppStream 2.0. For details on setting up SAML 2.0 integration, see the steps outlined at Setting Up SAML.

Q: Can I connect my users that are managed through User Pools to my Active Directory domain?

No. At this time we do not support User Pools users connecting to domain joined resources. To learn more about User Pools see, Using the AppStream 2.0 User Pool.

Q: How do my users sign in to streaming instances that are joined to an Active Directory domain?

When your users access a streaming instance through a web browser, they sign in to their Microsoft Active Directory domain by entering their domain password. When your users access a streaming instance by using the AppStream 2.0 client for Windows, they can either enter their Active Directory domain password or use a smart card that is trusted by the Active Directory domain. 

## Pricing and billing

Q: How much does Amazon AppStream 2.0 cost?

You are charged for the streaming resources in your Amazon AppStream 2.0 environment, and monthly user fees per unique authorized user accessing applications via Windows operating system based Amazon AppStream 2.0 streaming instance. You pay for these on-demand, and never have to make any long-term commitments.

The streaming resources consist of Amazon AppStream 2.0 instances in your Amazon AppStream 2.0 fleet as well as image builder instances. You have the option to have Always-On and On-Demand fleets. For Always-On fleets you pay for instances in your fleet that are running, even if users are not connected. These instances are billed per hour or per second based on the operating system and fleet type you select, and the price per hour is based on the instance type you select. For On-Demand fleets you pay for the instances in your fleet that are running only when a user is connected. These instances are billed per hour or per second based on the operating system you select, and the price per hour is based on the instance type you select. In an On-Demand fleet if an instance is running but not connected to a user, you pay a nominal hourly On-Demand Stopped Instance fee, which is the same for all instance types within a region. Image builder instances are only available as always on, and you pay for instances that are running, even if users are not connected. The charge for Always-On and On-Demand fleet instances as well as image builder instances includes the cost of the storage volumes used by the Amazon AppStream 2.0 image, and outbound bandwidth used by the streaming protocol. You can control the number of streaming instances in an Always-On or On-Demand fleet using fixed or dynamic scaling policies.

Elastic fleet streaming instances are billed per second with a minimum of 15 minutes for the duration of the streaming session, with a price per hour based on the instance type you select when creating the fleet.

The monthly user fee is used to pay for the Microsoft Remote Desktop Services Subscriber Access License (RDS SAL). This fee is charged per unique authorized user, and is charged in full (not pro-rated), regardless of when a user first accesses Amazon AppStream 2.0 in that month when streaming from a Microsoft Windows Server streaming instance. Schools, universities, and public institutions may qualify for reduced user fees. Please reference the Microsoft Licensing Terms and Documents for qualification requirements. If you think you may qualify, please contact us. We will review your information and work with you to reduce your Microsoft RDS SAL fee. There is no user fee incurred when using image builder instances or when streaming from Linux-based streaming instances.

You are charged separately for your usage of Amazon Simple Storage Service (S3) for any data stored within S3 buckets within your account.

Q: Can I bring my own licenses and waive the user fees?

Yes. If you have Microsoft License Mobility, you may be eligible to bring your own Microsoft RDS CAL licenses and use them with Windows based Amazon AppStream 2.0. For users covered with your own licenses, you won’t incur the monthly user fees. For more information about using your existing Microsoft RDS SAL licenses with Amazon AppStream 2.0, please visit this page, or consult with your Microsoft representative.

Q: What are the requirements for schools, universities, and public institutions to reduce their user fee?

Schools, universities, and public institutions may qualify for reduced user fees. Please reference the Microsoft Licensing Terms and Documents for qualification requirements. If you think you may qualify, please contact us. We will review your information and work with you to reduce your Microsoft RDS SAL fee. There is no user fee incurred when using image builder instances.

Q: What do I need to provide to qualify as a school, university, or public institution?

You will need to provide AWS your institution's full legal name, principal office address, and public website URL. AWS will use this information to qualify you for AppStream 2.0's reduced user fees for qualified educational institutions. Please note: The use of Microsoft software is subject to Microsoft’s terms. You are responsible for complying with Microsoft licensing. If you have questions about your licensing or rights to Microsoft software, please consult your legal team, Microsoft, or your Microsoft reseller. You agree that we may provide the information to Microsoft in order to apply educational pricing to your Amazon AppStream 2.0 usage.

Q. Does qualification for Amazon AppStream 2.0's reduced RDS SAL user fees affect other AWS cloud services?

No, your user fees are specific to Amazon AppStream 2.0, and do not affect any other AWS cloud services or licenses you have.

Q: Can I use tags to obtain usage and cost details for Amazon AppStream 2.0 on my AWS monthly billing report?

Yes. When you set tags to appear on your monthly Cost Allocation Report, your AWS monthly bill will also include those tags. You can then easily track costs according to your needs. To do this, first assign tags to your Amazon AppStream 2.0 resources by following the steps in Tagging Your AppStream 2.0 Resources. Next, select the tag keys to include in your cost allocation report by following the steps in Setting Up Your Monthly Cost Allocation Report.

Q: Are there any costs associated with tagging Amazon AppStream 2.0 resources?

There are no additional costs when using tags with Amazon AppStream 2.0.

## Compliance

Q: Is Amazon AppStream 2.0 HIPAA eligible?

Yes. If you have an executed Business Associate Addendum (BAA) with AWS, you can use Amazon AppStream 2.0 with the AWS accounts associated with your BAA to stream desktop applications with data containing protected health information (PHI). If you don’t have an executed BAA with AWS, contact us and we will put you in touch with a representative from our AWS sales team. For more information, see HIPAA Compliance. 

Q: Is AppStream 2.0 PCI Compliant?

Yes. Amazon AppStream 2.0 is PCI compliant and conforms to the Payment Card Industry Data Security Standard (PCI DSS). PCI DSS is a proprietary information security standard administered by the PCI Security Standards Council, which was founded by American Express, Discover Financial Services, JCB International, MasterCard Worldwide and Visa Inc. PCI DSS applies to all entities that store, process or transmit cardholder data (CHD) and/or sensitive authentication data (SAD) including merchants, processors, acquirers, issuers, and service providers. The PCI DSS is mandated by the card brands and administered by the Payment Card Industry Security Standards Council. For more information, see PCI DSS Compliance.

Q: Is Amazon AppStream 2.0 included in the System and Organizational Controls (SOC) reports?

Yes. Amazon AppStream 2.0 is included in the AWS System and Organizational Controls (SOC) reports. AWS System and Organization Controls Reports are independent third-party examination reports that demonstrate how AWS achieves key compliance controls and objectives. The purpose of these reports is to help you and your auditors understand the AWS controls established to support operations and compliance. You can learn more about the AWS Compliance programs by visiting AWS Compliance Programs or by visiting the Services in Scope by Compliance Program.