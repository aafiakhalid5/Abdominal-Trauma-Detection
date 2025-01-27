# Abdominal-Trauma-Detection

The goal of this project is to identify several potential injuries in CT scans of trauma patients. Any of these injuries can be fatal on a short time frame if untreated so there is great value in rapid diagnosis.

###  Files
*train.csv* Target labels for the train set. Note that patients labeled healthy may still have other medical issues, such as cancer or broken bones, that don't happen to be covered by the competition labels.

patient_id - A unique ID code for each patient.
[bowel/extravasation]_[healthy/injury] - The two injury types with binary targets.
[kidney/liver/spleen]_[healthy/low/high] - The three injury types with three target levels.
any_injury - Whether the patient had any injury at all.
