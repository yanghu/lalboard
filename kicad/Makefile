DOCS_DIR := ./docs
FAB_DIR := ./fab

all: main-stm cluster thumb-left thumb-right

main-stm:
	kicad-exports \
		-c automation/docs.kibot.lst \
		-c automation/fab.kibot.lst \
		-e main_stm.sch \
		-b main_stm.kicad_pcb

cluster:
	kicad-exports \
		-c automation/docs.kibot.lst \
		-c automation/fab.kibot.lst \
		-e cluster.sch \
		-b cluster.kicad_pcb

thumb-left:
	kicad-exports \
		-c automation/docs.kibot.lst \
		-c automation/fab.kibot.lst \
		-e thumb_cluster_left.sch \
		-b thumb_cluster_left.kicad_pcb

thumb-right:
	kicad-exports \
		-c automation/docs.kibot.lst \
		-c automation/fab.kibot.lst \
		-e thumb_cluster_right.sch \
		-b thumb_cluster_right.kicad_pcb

clean:
	rm -rf $(DOCS_DIR)
	rm -rf $(FAB_DIR)
	rm -f ./*.ogv
	rm -f ./*-docs-*.zip
	rm -f ./*-fab-*.zip
	rm -f ./*-drc.txt
	rm -f ./*-erc.txt
	rm -f ./*.csv
	rm -f ./kibot_errors.filter
