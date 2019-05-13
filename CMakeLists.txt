cmake_minimum_required(VERSION 3.12)
project(xgboost)

set(CMAKE_CXX_STANDARD 14)

include_directories(booster)
include_directories(booster/linear)
include_directories(booster/tree)
include_directories(regression)
include_directories(utils)

add_executable(xgboost
        booster/linear/xgboost_linear.hpp
        booster/tree/xgboost_base_treemaker.hpp
        booster/tree/xgboost_col_treemaker.hpp
        booster/tree/xgboost_row_treemaker.hpp
        booster/tree/xgboost_svdf_tree.hpp
        booster/tree/xgboost_tree.hpp
        booster/tree/xgboost_tree_model.h
        booster/xgboost-inl.hpp
        booster/xgboost.h
        booster/xgboost_data.h
        booster/xgboost_gbmbase.h
        regression/xgboost_reg.h
        regression/xgboost_reg_data.h
        regression/xgboost_reg_eval.h
        regression/xgboost_reg_main.cpp
        utils/xgboost_config.h
        utils/xgboost_fmap.h
        utils/xgboost_matrix_csr.h
        utils/xgboost_omp.h
        utils/xgboost_random.h
        utils/xgboost_stream.h
        utils/xgboost_utils.h)
