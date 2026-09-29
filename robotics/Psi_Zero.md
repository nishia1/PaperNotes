# Ψ₀: An Open Foundation Model Towards Universal Humanoid Loco-Manipulation
Link: https://psi-lab.ai/Psi0/
Code: https://github.com/physical-superintelligence-lab/Psi0

Ψ₀ suggests that rather than focusing on training humanoids on mass bulk amounts of data that we instead train a VLM on said data and then use it to post train a flow-based action expect on high quality humanoid robot data for join control. This method outperforms traditional systems trained on 10x data by 40% on various tasks.

# Demo Notes:
- Kitchen and Utility Skills: Has a good grasp on objects, able to reorient its position based on expected trajectories and appears to attempt to actually balance objects
- Cleanup & Scene Reset: Able to drop objects, so classify when fine-tuned motor control to get to desired position necessary versus simpler outcome of simply dropping the item

# General Notes:
- Trained on EgoDex for human videos in pretraining and Humanoid Everday for post training with the actual whole body actions
- Interesting use of  training time real-time chunking (RTC) which conditions each action prediction on previously comited action chunk to output consistent future action chunk with inference running asynch w exec to avoid chunk interruption
- Despite low amounts of data, outperforms most models including Groot! Significant improvements in task "Pull out the tray and turn to throw the chip can into the trash", "Pick the bottle, turn around, and pour into cup", and "Put the toy into the basket, turn around, and hand it over"

Interesting results that show that the full amount of data they used is quite necessary as when reduced, task effectiveness basically decreased but I wonder how the data would compare if this was reconducted with significantly more data!
