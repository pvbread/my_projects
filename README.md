# 🧬 Sequence Analysis & PDB Histogram Tools

This repository is a collection of Python tools and datasets for analyzing biological sequences (DNA/RNA) and exploring structural data in Protein Data Bank (PDB) files. It includes utilities for simulating restriction enzyme digestion and generating histograms from PDB files.

## 📂 Contents

### 🔬 Sequence Files
- `BC161026.fasta` / `BC161026.txt`: A nucleotide sequence that can be analyzed or used for in-silico digestion with restriction enzymes.
- `XM_002638640.fasta` / `XM_002638640.txt`: A second nucleotide sequence for analysis and comparison.
- `NM_002436.fasta`: A third nucleotide sequence, possibly a reference mRNA transcript.

### 🧪 Enzyme Digestion Simulations
- `BC161026_AatII`, `BC161026_AccII`, `BC161026_EcoRI`: These files represent the output of **in-silico digestion** of `BC161026` with respective restriction enzymes (AatII, AccII, EcoRI).
- `enzyme_sim.py`: A script to simulate how a given enzyme cuts a DNA sequence. Can be adapted to visualize or count fragments, or identify cleavage sites.
- `enzyme_test_file`: Likely a test input or config used by `enzyme_sim.py`.

### 🧬 Sequence Format Notes
All sequence files are in **FASTA or plain format**. These sequences could represent:
- Genomic DNA
- mRNA or cDNA transcripts
- Synthetic sequences for cloning or expression studies

## 🧱 Structural Analysis Tool

### `pdbHistogram.py`
A utility to analyze `.pdb` (Protein Data Bank) files and generate histograms of atoms or residues.

#### 📌 Usage
```bash
./pdbHistogram.py <your_pdb_file>
```

#### 🧰 Available Commands
| Command        | Description |
|----------------|-------------|
| `--help`       | Display help and usage instructions |
| `--total`      | Show total count of atoms and residues |
| `--atomhistogram` | Display a histogram of atom types |
| `--reshistogram`  | Display a histogram of residues |
| `--atominfo`      | Show detailed atom information |
| `--residueinfo`   | Show detailed residue information |

### Example Files
- `2JUU.pdb`: A sample PDB file you can analyze.
- `small.pdb`: A smaller PDB structure useful for testing or debugging.

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Make `pdbHistogram.py` executable:
   ```bash
   chmod +x pdbHistogram.py
   ```

3. Run:
   ```bash
   ./pdbHistogram.py 2JUU.pdb --atomhistogram
   ```

4. Simulate restriction digests using `enzyme_sim.py`:
   ```bash
   python enzyme_sim.py BC161026.fasta EcoRI
   ```
