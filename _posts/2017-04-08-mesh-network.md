---
title: "Mesh Network"
tags: [coding club, projects]
---


Before we even get started, what *is a mesh network*?

The best analogy for a mesh network is the cellphone network. We all use cell phones in our daily lives and know that they work by communicating to one another through cell towers.

For example let's explore the following scenario: Alice wants to send a text to Bob using her cellphone:

1. Alice uses her phone to send a text to `123` which is Bob's cell phone number
2. Alice's phone sends the text as well as the number `123` to the nearest cell phone tower, lets call this `Tower A`
3. `Tower A` then sends the message to `Tower B` because Bob isn't in the range of `Tower A`
4. `Tower B` receives the text message from `Tower A` as well as the number `123` which was also sent.
5. `Tower B` forwards the text to Bob's phone since it knows that Bob has the number `123`

Clearly, this is extremely simplified. But it explains the idea fairly well.

Then a mesh network is a collection of *devices* and *nodes*. In our instance the *nodes* are the "cell phone towers" which receive messages from the *devices* and forward them to other *nodes* until a node is reached that is able to directly the message to the targeted *device*. The cool thing with this is you can really send your messages very far!

Let's image this: A single *node* can only send a message within a range of 100 meters, but Bob is 300 meters away from Alice. So then how does Alice send a message to Bob?

The answer is that Alice simply sends her message to the nearest node, which then *relays* the message to another node, and another and another until it finds a node which is close enough to Bob so that it can directly send it to Bob.

### Project

Your project is to work together in a team to design a private, encrypted mesh network for the school. That means first you need to decide what each of your roles are. Once you have that decided you will each need to go off and learn about your roles.

The **Arduino Developers** need to focus on learning about how Arduino's are programmed. They specifically should follow the [Sparkfun Inventor's Guide][SIK]. Speak to Mr. Clements about getting access to the kits. 

The **Electronics Designer**also needs to work through the Guide linked above, but pay special attention to the electronics instead of the code. You will also need to learn about the wireless receiver transmitter two in one module we are using. It's called [Nrf24L01][RADIO] and it has a [theoretical][FIX_RANGE] range of 1000m. Work together with the **Arduino Developers** to follow this [tutorial][TUTORIAL] that explains how to hookup the radios and get them working

The **Research and Development** team should in the meantime be working on researching the information from this post and figuring out other important resources that would be helpful. This may inlude things like tutorials on the Arduino platform, explanations of radio communications or even a video of that explains how mesh networks work. You will also be involved in researching new ideas we can use, such as solar powered nodes.

The **Structural Designer** should be focusing on designer some sort of enclosure using [TinkerCAD][TINKERCAD] that would allow us to safely store our finished *nodes* around the school building in a safe box. The goal is to figure out a design that doesn't interfere with the radio signals, and has the space for an LCD screen. Take a look inside the SparkFUN kit's to measure the dimensions of the LCD Screen. Don't worry too much about actually getting the LCD screen to work as we will focus on that once I'm back!

Lastly, the role of the **Secretary** is to not be told what to do! Ha, your job is to figure out all the planning in the meantime while I'm away. But here are some tips:

- Keep a record of what each member accomplishes throughout the week
- Keep a section dedicated to possible ideas, such as solar power
- Always ask for new ideas, and feedback from the other members
- Set tasks for each week. For example the task for the first for the Arduino Developers might be to work through Lesson 1 - 10 from the SparkFun Inventor's Guide
- If you think an idea has gone on for long enough and doesn't seem to be going anywhere then feel free to reassign the member on that task to something else! So let's say if we can't figure out away to fit the LCD screen in a closed box, then ask them if they can instead design something with a hole for a status led

### Materials
- Sparkfun Arduino Kits (2)
- Radio Transmitter Receivers (2) : [Nrf24L01+][RADIO]

### Roles
* As the roles are taken, they will be checkmarked *

- [ ] **Arduino Developer** :  Involves learning about the Arduino and working through the SparkFun guide book. You will be responsible for most of the coding!
- [ ] **Arduino Developer** : Involves learning about the Arduino and working through the SparkFun guide book. You will be responsible for most of the coding!
- [ ] **Electrical Design**: You will be working in cooperation with the Arduino developers to figure out the electronics. So I recommend instead of taking out a Sparkfun, work on the electronics circuits with the coders. That way you can focus on understanding how the electronics works, and let the others deal with the code.
- [ ] **Research and Development**: While the others are working on learning the skills to create the mesh network, we need someone actually researching mesh networks and working on plan to make the entire product work together!
- [ ] **Research and Development**: While the others are working on learning the skills to create the mesh network, we need someone actually researching mesh networks and working on plan to make the entire product work together!
- [ ] **Structural Design**: Your main role will be figuring out how to make the whole product fit together, literally! So spend some time learning about 3D Printers and try some basic 3D Design. Checkout [TinkerCAD][TINKERCAD] for a simple but powerful modeller.
- [ ] **Deputy Leader / Secretary**: Okay now this might not sound super exciting, but it is! Behind every engineering team is a leader who keeps everyone on track. Your role involves making sure that everyone shows up to meetings and to check what their current progress is. I need you to keep record of meeting discussions and to make sure everyone is accomplishing tasks. Essentially you are the boss and can assign tasks to the other members. For example, let's say you have figured out that a particular design using the Arduino at 8 MHz (the speed of the processor) [^1] is fast enough, even though 16 MHz will be even faster. Then you can speak to the **Electrical Designer** and ask them to make sure their circuit is able to power the lower power 8 MHz, in this case it means that they need to replace their 5V battery for a 3V Battery[^2].

## Follow up
As we get farthter into the project, I will be publishing more information. For the time being all discussions of ideas will occur on the Hangouts chat and will be recorded in the document, to be created by the **Secretary**


[SIK]: https://cdn.sparkfun.com/datasheets/Kits/SFE03-0012-SIK.Guide-300dpi-01.pdf
[RADIO]: https://arduino-info.wikispaces.com/Nrf24L01-2.4GHz-HowTo
[FIX_RANGE]: http://hackaday.com/2016/05/31/fixing-the-terrible-range-of-your-cheap-nrf24l01-palna-module/
[TINKERCAD]: https://tinkercad.com
[TUTORIAL]: https://arduino-info.wikispaces.com/Nrf24L01-2.4GHz-HowTo

[^1]: Just like a computer processor, the microcontrollers run at a certain speed. Unlike desktops which run in the range of 2 - 3 GHz, microcontrollers run in MHz. What you need to understand is simply that running at a higher frequency requires more energy. So if the product can be designed to work at 1 MHz for the highest efficiency then it will also use up the least amount of power!

[^2]: The Arduino has two power options : 3.3 V and 5.0V. The 3.3V is lower power and is used when running the processor at 8 MHz, but running it at a higher 16 MHz requires 5.0V of power.
