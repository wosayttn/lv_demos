import rtconfig

from building import *

demo_src_folder = ''
cwd = GetCurrentDir()+'/src'

if GetDepend('PKG_USING_LV_DEMO_MUSIC'):
    demo_src_folder = 'src/lv_demo_music'

if GetDepend('PKG_USING_LV_DEMO_STRESS'):
    demo_src_folder = 'src/lv_demo_stress'

if GetDepend('PKG_USING_LV_DEMO_WIDGETS'):
    demo_src_folder = 'src/lv_demo_widgets'

if GetDepend('PKG_USING_LV_DEMO_KEYPAD_ENCODER'):
    demo_src_folder = 'src/lv_demo_keypad_encoder'

if GetDepend('PKG_USING_LV_DEMO_BENCHMARK'):
    demo_src_folder = 'src/lv_demo_benchmark'

CPPPATH = [ cwd ]
src = Glob(demo_src_folder+'/*.c')
src += Glob(demo_src_folder+'/assets/*.c')

group = DefineGroup('LVGL-demo-music', src, depend = ['PKG_USING_LV_DEMO_MUSIC'], CPPPATH = CPPPATH)
group = DefineGroup('LVGL-demo-stress', src, depend = ['PKG_USING_LV_DEMO_STRESS'], CPPPATH = CPPPATH)
group = DefineGroup('LVGL-demo-widgets', src, depend = ['PKG_USING_LV_DEMO_WIDGETS'], CPPPATH = CPPPATH)
group = DefineGroup('LVGL-demo-keypad-encoder', src, depend = ['PKG_USING_LV_DEMO_KEYPAD_ENCODER'], CPPPATH = CPPPATH)
group = DefineGroup('LVGL-demo-benchmark', src, depend = ['PKG_USING_LV_DEMO_BENCHMARK'], CPPPATH = CPPPATH)

Return('group')
