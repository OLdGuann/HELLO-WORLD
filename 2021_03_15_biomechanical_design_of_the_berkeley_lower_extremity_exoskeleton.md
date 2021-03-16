@def class = "journal"
@def authors = "Zoss, A.B.; Kazerooni, H.; Chu, A.;"
@def title = "Biomechanical Design of the Berkeley Lower Extremety Exoskeleton (BLEEX)"
@def venue = "IEEE; ASME Transactions on Mechatronics"
@def year = "2006"
@def hasmath = true
@def review = true
@def tags = ["reviews","exoskeleton","biomechanics","mechatronics","robotics"]
@def reviewers = ["Guan Huitao","David Yackzan"]

\toc
### Broad area/overview
This paper describes the design of an exoskeleton to be worn from hip down (lower extremety) on an individual to assist in the transportation of heavy objects. The strength of lower extremety exoskeletons is that in combination with human intelligence and control, they can aid in the transportation of heavy objects over terrain that is not navigable by wheeled robots (like stairs or rocky terrain) as well as over non-simple pathways that will take human decision and control to navigate.

### Notation
* $x$: state, $X$: State space
* $y$: measurement, $Y$: Measurement Space
* Controller $u = g(y)$
* $L$: Set of labels
* $C_X \colon X \to L$: Classifier in state space
* $C_Y \colon Y \to L$: Classifier in measurement space
* $V$: Lyapunov function
* $W$: set of hyperplanes that parametrizes $C_X$
* $W^\Delta$: set of hyperplanes that parametrizes a robust version of $C_X$

### Specific Problem
* This design outlined in this paper focuses on providing the goal of allowing its wearer to carry significant loads without expending much effort over any terrain while considering four primary aspects: "a novel control scheme, high-powered compact power supplies, special communication protocol and electronics, and a design architecture to decrease the complexity and power consumption."

### Solution Ideas
* A control scheme was designed that allows the BLEEX exoskeleton to shadow the wearers movements, both voluntary and involuntary.
* In order to acheive this, the system uses a full dynamic model of the exoskeleton as it retrieves data from several sensors (encoders, linear accelerometers, single axis force sensors, foot switches, load distribution sensors, and an inclinometer) and actively calculates the kinematics of the skeleton.
* This exoskeleton includes 7 DoF in total:
  - 3 DoF at the hip
  - 1 DoF at the knee
  - 3 DoY at the ankle
* The control scheme consists of a power efficient method of only actuating the joints that require the most assistance during weighted locomotion, while the other joints are free or attached with a spring to allow for natural motion of the wearer and constant assistance in a preferred direction. The joints to be actuated were identified through locomotion observation trials and are as follows:
  - flexion/extension at the ankle
  - flexion/extension at the knee
  - flexion/extension at the hip
* The following equations were considered in determining the size and strength of the hydraulic actuators:
  - $T_maxpush = Ps * \frac{\pi*D_bore^2}{4}*R(\theta)$
  - $T_maxpull = Ps * \frac{\pi*D_bore^2-D_rod^2}{4}*R(\theta)$
  - Where $D_bore$ is the actuator bore diameter and $D_rod$ is the actuator rod diameter.

### Comments


### Recent Papers
* This paper, titled *Physical Human–Robot Interaction of a Robotic Exoskeleton By Admittance Control* outlines a more recent approach to design of a human-assistive exoskeleton: https://saa-primo.hosted.exlibrisgroup.com/primo-explore/fulldisplay?docid=TN_cdi_crossref_primary_10_1109_TIE_2018_2821649&context=PC&vid=UKY&lang=en_US&search_scope=default_scope&adaptor=primo_central_multiple_fe&tab=default_tab&query=any,contains,exoskeleton&offset=0
