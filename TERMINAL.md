cd "/home/riccardo/Desktop/RDX V-JEPA2.1 > DINOv2 ViT-g"
python3 run_rdx_comparison.py

cd "/home/riccardo/Desktop/RDX V-JEPA2.1 > DINOv2 ViT-g/RDX"
python3 interactive_cluster_viz_general.py \
  --rdx_output_dir "../rdx_output/dinov2_vs_vjepa21/rdx_nb_lb_spectral" \
  --repr_0_path    "../rdx_output/dinov2_vs_vjepa21/m0_rep.pkl" \
  --repr_1_path    "../rdx_output/dinov2_vs_vjepa21/m1_rep.pkl" \
  --repr_0_name    "DINOv2 ViT-g14" \
  --repr_1_name    "V-JEPA2.1 Gigantic" \
  --image_paths    "../rdx_output/dinov2_vs_vjepa21/image_paths.pkl" \
  --data_root      "../corpus" \
  --output_path    "../rdx_output/dinov2_vs_vjepa21/index.html"

cd "/home/riccardo/Desktop/RDX V-JEPA2.1 > DINOv2 ViT-g/rdx_output/dinov2_vs_vjepa21"
python3 -m http.server 8787
