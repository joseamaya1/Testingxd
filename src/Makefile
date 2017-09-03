TFS = tfs

INCLUDEDIRS = -I"." -I"/usr/include/luajit-2.0" -I"/usr/include/mysql"

FLAGS = -DBOOST_DISABLE_ASSERTS -DNDEBUG

CXXFLAGS = -march=native -mtune=native $(INCLUDEDIRS) $(FLAGS) -Werror -Wall -Ofast -g -std=c++11 -lpthread
CXX = g++

LIBS = -lluajit-5.1 -lgmp -lboost_system -lmysqlclient /usr/lib/libtcmalloc_minimal.so.4

LDFLAGS = $(LIBS)

CXXSOURCES = actions.cpp \
account.cpp \
ban.cpp \
baseevents.cpp \
bed.cpp \
chat.cpp \
combat.cpp \
commands.cpp \
condition.cpp \
configmanager.cpp \
connection.cpp \
container.cpp \
creature.cpp \
creatureevent.cpp \
cylinder.cpp \
database.cpp \
databasemanager.cpp \
databasetasks.cpp \
depotchest.cpp \
depotlocker.cpp \
events.cpp \
fileloader.cpp \
game.cpp \
globalevent.cpp \
groups.cpp \
guild.cpp \
house.cpp \
housetile.cpp \
inbox.cpp \
ioguild.cpp \
iologindata.cpp \
iomap.cpp \
iomapserialize.cpp \
iomarket.cpp \
item.cpp \
items.cpp \
luascript.cpp \
mailbox.cpp \
map.cpp \
monster.cpp \
monsters.cpp \
mounts.cpp \
movement.cpp \
networkmessage.cpp \
npc.cpp \
otpch.cpp \
otserv.cpp \
otpch.cpp \
outfit.cpp \
outputmessage.cpp \
party.cpp \
player.cpp \
position.cpp \
protocol.cpp \
protocolgame.cpp \
protocollogin.cpp \
protocolold.cpp \
protocolstatus.cpp \
protocolspectator.cpp \
protocolgamebase.cpp \
quests.cpp \
raids.cpp \
rewardchest.cpp \
reward.cpp \
rsa.cpp \
scheduler.cpp \
scriptmanager.cpp \
server.cpp \
spawn.cpp \
spells.cpp \
store.cpp \
talkaction.cpp \
tasks.cpp \
teleport.cpp \
thing.cpp \
tile.cpp \
tools.cpp \
trashholder.cpp \
vocation.cpp \
waitlist.cpp \
weapons.cpp \
wildcardtree.cpp

OBJDIR = obj
CXXOBJECTS = $(CXXSOURCES:%.cpp=$(OBJDIR)/%.o)

all: $(TFS)

clean:
	$(RM) $(CXXOBJECTS) $(TFS)

$(TFS): $(CXXOBJECTS)
	$(CXX) $(CXXFLAGS) -o $@ $(CXXOBJECTS) $(LDFLAGS)

$(OBJDIR)/%.o: %.cpp
	$(CXX) -c $(CXXFLAGS) -o $@ $<

