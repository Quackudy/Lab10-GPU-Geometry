Lab 10 — Student ID 6732029421

Prepared: four student source files; hello, shaded trace, steps, k=0 and k=1
images; freshly generated 1000-triangle 6732029421.obj; CPU generation logs;
AI prompt log; wireframe preview (not the required viewer screenshot).

DO BEFORE SUBMISSION
1. Run from the repository root:
   make check
   make hello
   make simplify ARGS="--target 1000"
   make metric ARGS="data/part.obj out/simplified.obj"
   make judge ARGS="submission/6732029421/6732029421.obj"
   Save the judge output in this package's logs/judge.txt.

2. For the server timing question, push/pull your source, then on the login node:
   make -f Makefile.gpu
   mkdir -p out
   sbatch --export=ALL,PROGRAM=trace,ARGS="--compare" slurm/run.sbatch
   squeue --me
   Read out/lab10-<jobid>.out after the job finishes. Verify it names a GPU.
   Record CPU single ms, Render ms, and their ratio yourself.

3. Open 6732029421.obj in Blender or another 3D viewer. Enable wireframe/edges,
   rotate and frame the mesh so its hole and bump are visible. Save a screenshot
   as pictures/mesh_wireframe_viewer.png. The included Matplotlib preview does
   not replace the viewer screenshot required by the handout.

4. Write your own short answers from handout pages 3, 8, 11 and 12:
   - Threads versus pixels and why they can differ.
   - Server CPU/GPU timings and speedup.
   - Bright regions in steps mode and why grazing rays need more steps.
   - Your observation comparing trace_k0.png and trace_k1.png.
   - Where triangles remain after simplification and why.
   - V, E, F and chi before/after, and whether chi changed.
   - Which metric direction took longer and why (samples x target triangles).
   Put these in your report; no measured answers have been supplied for you.

5. Competition generating command (already run from repository root):
   ./build/simplify --target 1000 --out submission/6732029421/6732029421.obj
   Include this command and the judge line from your own test in your report.

6. Complete student name, prior-knowledge fields and your checks in
   AI_PROMPT_LOG.md; add earlier AI sessions if any and remove unused template.
   Inspect all pictures before submitting.

7. Add your report, viewer screenshot and judge log, then recreate the ZIP:
   python3 -c "import shutil; shutil.make_archive('submission/6732029421','zip','submission','6732029421')"

Images were generated using CPU emulation. CPU generation logs are not GPU
measurement evidence. Source copies reflect the files at package creation;
recopy student/*.cu if you edit code afterward and regenerate affected outputs.
