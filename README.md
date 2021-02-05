# comp4102-project

<b>Title:</b> Physical to Digital Dice Roll; Ethan Thompson

<b>Summary:</b> User will roll a dice in front of a camera and the results of the roll would be printed to the screen by the system. Primarily for use in tabletop games such as D&D where some players would rather use physical dice over digital dice, as this would allow for a hybrid making it easier for groups to play remotely.

<b>Background:</b> Due to the covid pandemic, social gatherings have been restricted which makes tabletop games much more difficult to play in groups. Many digital tools have already been created to facilitate the playing of games such as D&D remotely, however they tend to employ digital dice rolling as part of their system. Most players, from my experience, prefer to use physical dice from their collection that they have worked on through the years. I would like to create a system to facilitate the use of physical dice in a virtual capacity, and hopefully build on and add to the already existing tools that facilitate the collection of resources for the game.

<b>The Challenge:</b> This problem can be challenging, as it will involve reading digits from dice at different angles, illuminations, as well as different dice textures and opacities. In addition to the traditional D6 (a dice with 6 sides) the system will also need to be able to read the results of rolls from D2's, D4's, D8's, D10's, D12's, and of course D20's. Additionally, the system will need to be able to use object recognition to recognize what is and is not accepted as dice.

<b>Goals and Deliverables:</b> If the system can read the results of the rolled dice and correctly output them to the user, this is a success. In this case, a success is easily measurable, as the results of the rolled dice are easily read by the human eye in real time.

    Plan to Achieve:
    - A system that can correctly detect and recognize a valid die.
    - A system that can correctly read the results after the dice are rolled.
    - A system that can correctly output the results of the roll to the user.
    - A system that can read the results of a dice roll correctly for a moderate range of dice size, texture,
      and opacity.

    Hope to Achieve (in order of preference):
    - A system that can provide the results of the roll as a sum of the dice or as multiple different rolls
      (example: in D&D usually when you roll 2 D20's you do not want the sum of the 2 dice rolls, but rather
      the results from each individual die so you can use the higher or lower number depending on the
      situation)
    - A system that can read the results of a dice roll correctly for a wide range of dice size, texture,
      and opacity.
    - Integrate the system with a pre-existing tool (such as Roll20.net, DnDBeyond.com, or hopefully the
      Beyond20 extension that links the former two) so that any modifiers dictated by the game can be added
      to the results of the roll
    - Construct a physical dice rolling tower than houses the camera used by the system, and allows users
      to drop dice into the top and when they come out the system will be able to start the processing
      the results.

<b>Schedule:</b>
*ALL tasks are to be completed by the sole team member, Ethan Thompson

    Week 1 (February 7th):
    - Begin work on project code base for uses such as camera device interface/ data exchange, image data
      storage, etc.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 2 (February 14th):
    - Complete work on project code base (specified in Week 1).
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 3 (February 21st):
    - Begin dice object detection and specification for accepted dice. This will involve determining the
      face that has the value considered as the result (the top face), as this can differ slightly
      depending on the rolled die. (D4 dice do not usually have the traditional flat top that has the value
      of the roll)
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 4 (February 28th):
    - Complete dice object detection and specification for accepted dice.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 5 (March 7th):
    - Begin dice result processing functionality. This involves reading the printed value on the die face
      and in most cases summing the values.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 6 (Marth 14th):
    - Complete dice result processing functionality.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 7 (March 21st):
    - Complete result output functionality.
    - Begin testing with different dice size, texture, and opacity. Make adjustments to accommodate as
      needed.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 8 (March 28th):
    - Complete testing and adjustments for different dice size, texture, and opacity.
    - Begin testing in different environments with different lighting. Make adjustments to accommodate as
      needed.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 9 (April 4th):
    - Complete testing and adjustments for different environments with different lighting.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
    
    Week 10 (April 11th):
    - Prepare for demo and presentation.
    - At the end of the week, test and review code as well as ensure proper documentation is being kept.
