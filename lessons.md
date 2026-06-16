
# Week 1

# From the materials
Video Note:Understood that LLMs are next token predictors and can memorize biological facts but struggle with precise mathematical or genomic coordinate arithmetic.
Reflection:Tasks like searching for public gene IDs are easy for LLMs, but writing custom scripts to parse messy FASTQ data requires careful code validation because the LLM might hallucinate syntax.

# Surprises
ChatGPT Asked it to find the sequence length of human GAPDH gene. It gave a plausible number but mixed up cDNA length with genomic locus length. Takeaway:Always double-check sequence lengths from LLMs against official NCBI databases.

# Week 2

# From the materials
Video Note:Learned about the ReAct framework where agents think, act, and observe. It is crucial to give agents good tools (like compilers and bash access) to minimize errors.
Reflection: Feature engineering requires domain knowledge. If we don't guide the agent on biological invariants, it will write code that runs perfectly but produces scientifically useless metrics.

# Surprises
Antigravity agent Asked the agent to fix a broken script parsing a GFF3 file. The agent fixed the syntax error and the script ran, but it silently skipped the header lines incorrectly. Takeaway:Spot-check data rows before and after agent modifications.

# Week 3

# From the materials
Video Note: Watched the lecture on Bio Foundation Models. Genomic LMs are powerful for zero-shot variant effect prediction but require proper benchmarking against published baselines.
Reflection:When evaluating a genomic model on Genomic Benchmarks, the input formatting (like 0-based vs 1-based coordinates) changes the output entirely.

# Surprises
Claude Asked it to write a script using `fetch_proteins.py` to pull FASTA sequences. It forgot to handle API rate-limiting, and the NCBI server blocked the requests halfway through. Takeaway: Tell the agent to add sleep delays when fetching bio data from public APIs.

