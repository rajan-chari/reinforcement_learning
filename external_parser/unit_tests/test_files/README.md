## How test files were generated

- cb_v2.fb: `./example_gen --kind cb --count 1`
- f-reward_v2.fb: `./example_gen --kind f-reward --count 1`
- cb_simple.log: generated by running `python joiner.py --problem_type_config 1` on the above files (cb_v2.fb, f-reward_v2.fb).
- cb_v2_dedup.fb: `./example_gen --kind cb --count 1 --dedup`
- cb_dedup_compressed.log: generated by running `python joiner.py --problem_type_config 1` with cb_v2_dedup.fb and f-reward_v2.fb
- cb_v2_size_2.fb: `./example_gen --kind cb --count 2`
- f-reward_v2_size_2.fb: `./example_gen --kind f-reward --count 2`
- bad_magic.log, bad_version.log, no_msg_hdr.log, empty_msg_hdr.log unknow_msg_type.log, and bad_joined_payload.log were generated by running `python joiner.py -c --problem_type_config 1` with the files (cb_v2_size_2.fb, f-reward_v2_size_2.fb)

### reward function test files
- reward_functions/cb_v2.fb: `./example_gen --kind cb --count 1 --seed -1`
- reward_functions/cb_apprentice_match_baseline_v2.fb: `./example_gen --kind cb --seed -1 --apprentice`
- reward_functions/f-reward_3obs_v2.fb: `./example_gen --kind f-reward --count 3 --seed -1 --random_reward`
