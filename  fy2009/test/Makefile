include ../Make.defines

INC_FLAG=-I../h
PATH_LIB= ../lib
PATH_BIN=bin
PATH_OBJS=./objs

###################################################
all:base stm msg aio thd rawsok sok
 
clean:clean_base clean_stm clean_msg clean_aio clean_thd clean_rawsok clean_sok
###################################################
#test base,2006-7-13
base:fyt_base.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -DFY_ENABLE_ASSERT -lpthread -g -o $(PATH_BIN)/$@ fyt_base.cpp $(PATH_LIB)/fy_util.a

#test stream
stm:fyt_stream.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -DFY_ENABLE_ASSERT -lpthread -g -o $(PATH_BIN)/$@ fyt_stream.cpp $(PATH_LIB)/fy_util.a

#test message
msg:fyt_msg.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -DFY_ENABLE_ASSERT -lpthread -g -o $(PATH_BIN)/$@ fyt_msg.cpp $(PATH_LIB)/fy_util.a

#test aio 2008-6-18
aio:fyt_aio.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -lpthread -o $(PATH_BIN)/$@ fyt_aio.cpp $(PATH_LIB)/fy_util.a

#test thread features,2006-8-14,usa
thd:fyt_thd.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -lpthread -o $(PATH_BIN)/$@ fyt_thd.cpp $(PATH_LIB)/fy_util.a

#test rawsok 2009-8-27
rawsok:fyt_rawsok.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -lpthread -o $(PATH_BIN)/$@ fyt_rawsok.cpp $(PATH_LIB)/fy_util.a

#test sok 2008-10-9
sok:fyt_sok.cpp
	$(CXX) $(DEFAULT_FLAGS) $(INC_FLAG) -lpthread -lssl -o $(PATH_BIN)/$@ fyt_sok.cpp $(PATH_LIB)/fy_util.a
###################################################
###################################################
clean_base:
	(rm -f $(PATH_BIN)/base)
clean_stm:
	(rm -f $(PATH_BIN)/stm)
clean_msg:
	(rm -f $(PATH_BIN)/msg)
clean_aio:
	(rm -f $(PATH_BIN)/aio)
clean_thd:
	(rm -f $(PATH_BIN)/thd)
clean_rawsok:
	(rm -f $(PATH_BIN)/rawsok)
clean_sok:
	(rm -f $(PATH_BIN)/sok)

