# Clone SNAP GitHub repository
git clone https://github.com/open-power/snap
cd snap
make software actions
# Find available card
./software/tools/snap_find_card -A ADKU3
# SNAP Action discovery
./software/tools/snap_maint -v 
# Running hls_helloworld
cd $HOME/snap/actions/hls_helloworld/sw
echo "Hello World. I love this new experience with SNAP." > /tmp/t1
./snap_helloworld -i /tmp/t1 -o /tmp/t2
