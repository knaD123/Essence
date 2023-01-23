# Essence
Essence reproducibility package
README
Introduction
This is a tool for simulating network topologies and failure scenarios. It can be used to test different algorithms and configurations to determine their effectiveness in restoring network connectivity in the event of a failure.

Installation
Clone the repository to your local machine.
Install the required packages by running pip install -r requirements.txt
Usage
To run the tool, you first need to create a configuration for a topology. You can do this by running python3 create_confs.py --keep_failure_chunks --topology ${TOPO} --conf confs --result_folder results --threshold 100 --algorithm rsvp-fn. Replace ${TOPO} with the desired topology.
To run the essence algorithm, you need to specify the number of generations and population size.
Finally, to run the tool, use the command python3 tool_simulate.py --conf ${CONFIG} --failure_chunk_file "confs/${TOPO}/failure_chunks/${FAILCHUNK}" --flows_file "confs/${TOPO}/flows/${FLOWS}". Replace ${CONFIG}, ${TOPO}, ${FAILCHUNK} and ${FLOWS} with the appropriate values.
