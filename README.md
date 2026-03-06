# Agentic AI Driven Online Exam Proctoring System

I developed a real-time AI-based online exam proctoring system using MediaPipe FaceMesh and OpenCV. The system monitors students during online exams through webcam input. It detects multiple faces, face absence, and head movements by analyzing facial landmarks. If suspicious behavior is detected repeatedly, the system triggers warnings and automatically terminates the exam. This project demonstrates my understanding of computer vision, real-time processing, and AI-based monitoring systems.

Agentic AI-Driven Online Proctoring System. Most current proctoring tools just record video for later review. My project is different: it is an Autonomous Agent that monitors, reasons, and acts in real-time to ensure exam integrity without needing a human proctor present."

## The Core Architecture 
"I have designed this system using a Multi-Agent Architecture consisting of four specialized modules:

The Vision Agent: Uses MediaPipe to track 468 facial landmarks. It calculates the head's position using Scale-Invariant Logic, meaning it stays accurate whether the student is close to or far from the camera.

The Memory Agent: Tracks the history of the student’s behavior. It doesn't just look at one frame; it remembers what happened 2 seconds ago.

The Generative Reasoning Agent: This provides a human-readable explanation of why a behavior is risky—for example, explaining that a left turn might indicate an off-screen reference.

The Action Agent: This is the 'enforcer.' It manages warnings and executes the Termination Protocol if the rules are repeatedly broken."

## The Live Demo (Point these out while running the code)
Show the Normal State: "As you can see, while I am looking at the screen, the status is 'Safe' and the box is green."

Show the Intent Reasoning (The Timer): "Now watch: if I glance away quickly to sneeze, the system notices, but it does not give me a warning. It uses a Temporal Buffer to analyze my intent. It only counts it as a violation if I look away for more than 1.5 seconds."

Show the Warning & Action: "If I continue to look away, the Action Agent triggers a beep and issues a warning. After 3 such incidents, the agent autonomously decides the exam is compromised and terminates the session."

## The Conclusion (The "Business Value")
"Finally, the system doesn't just stop. It generates a Proctoring Evidence Log (CSV). This file contains every timestamp and violation type, providing a clear audit trail for the examiners. This project moves AI from a passive observer to an active, reliable decision-maker."
