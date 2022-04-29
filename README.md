# EasyConsoleTool

      A TCL VMD Program for the easy and flexible trajectory analysis.

 **AUTHOUR**  
        
      ANJI BABU KAPAKAYLA
      IIT KANPUR, INDIA.
      anjibabu480@gmail.com

 **USAGE**
           
      source ECT.tcl in VMD tk console
           
 **Commands available**
          
     my_commnds: Prints available commands on the console
     Alignment, RMSD ,distance, angle, dihedral, contact_map
     clustering, details, count_waters, HBonds, pbs_box, 
     save_pdb, save_image, sasa, save_coordinates, bgcolor
     HB_occupancy, show_interactions, show_hbonds,count_hbonds
     --help
 
 **Examples**
            
     my_commands   : Shows all available commands
   
 **--help** 
      
      Gives details of any mentioned command
      USAGE   : --help command
      example : --help distance
      example : --help angle
**save_pdb** 

      Writes pdb file for given options
      USAGE : save_pdb atomselection start_frame end_frame stride molid filename
      EXAMPLE  : save_pdb "protein" 5 100 5 top file.pdb
      Above example , It will write file.pdb for "protein" from frame 5 to 100 by skipping every 5 frames.
**Align** 
      
      align molid1 molid2
      example   : align 0 1
      
**RMSD**
      
      Measures Avg.RMSD & std for given selections
      USAGE    : rmsd Atomselection molid1  molid2
      example  : rmsd "backbone" top  1
      example  : rmsd "protein" top top
      IF both the molids are same , RMSD will be calculated by taking zeroth frame as reference

**distance**

      Measures Distance, Avg Distance & std for any given 2 atoms
      USAGE    : distance sel1 sel2 <initial-frame> <end-frame> <-show_plot>
      example  : distance "serial 3418" "serial 3415" 
      example  : distance "serial 3418" "serial 3415" 100 2000
      example  : distance "serial 3418" "serial 3415" -show_plot
      example  : distance "serial 3418" "serial 3415" 10 1000 -show_plot
      OUTPUT   : DISTANCE.xvg and dist.png

**angle** 

      Measures Avg. angle & std  for any given 3 atoms
      USAGE    : angle sel1 sel2 sel3
      example  : angle "serial 3418" "serial 3415" "serial 3395"
      OUTPUT   : ANGLE.dat

**dihedral**
      
      Measures Avg Dihedral angle & std  for any given 4 atoms 
      USAGE    : dihedral sel1 sel2 sel3 sel4
      example  : dihedral "serial 3418" "serial 3415" "serial 3412" "serial 3395"
      example2 : dihedral "index 3417" "index 3414" "index 3411" "index 3394"
      OUTPUT   : DIHEDRAL.dat

**show_residues**
      
      Prints RESID and corresponding RESNAME for given selection and for given frames
      USAGE    : show_residues sel molid <initial frame>  <final frame>
      example  : show_residues "resid 170 to 180" 0 0 5
      example2 : show_residues "(not resname WAT) and within 3 of resid 235" 0 5 10
      example3 : show_residues "protein and hydrophobic " 0 1 0
      OUTPUT   : RESNAMES.dat

**details**

      Prints required molecular details for given molid
      USAGE    : details molid
      example  : details 0

**count_waters**

      Prints Avg. No of waters present around given selection
      USAGE    : count_waters sel molid start_frame end_frame
      Example  : count_waters "within 5 of resid 235" 0 5 10
      OUTPUT   : NO-OF-WATERS.dat

---
**Anji Babu Kapakayala**


    
  
     
