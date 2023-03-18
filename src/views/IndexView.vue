<style>
.layout-base {
    background-color: #fff !important;
    margin-left: 15%;
    margin-right: 15%;
}

.layout-header {
    background: #fff !important;
    background-color: #fff !important;
    /* background-image: url(../assets/testbg2.png) !important; */
    /* background-repeat:no-repeat !important;
    background-size: 100% 100% !important; */
    height: 90px !important;
    min-height: 10px !important;
    padding: 0px !important;
    margin-top: 10px !important;
    margin-left: 0px !important;
    /* font-family: 'Times New Roman', Times, serif; */
    /* padding-left: 10px !important; */
}

.layout-sider {
    background-color: #fff !important;
    min-width: 30% !important;
    height: 100%;
}

.layout-content {
    background-color: #fff;
    min-height: 400px;
}

.layout-center {
    background-color: #fff !important;
    font-family: iowan old style, ovo, hoefler text, Georgia, times new roman, tibch, source han sans, pingfangsc-regular, hiragino sans gb, stheiti, microsoft yahei, droid sans fallback, wenquanyi micro hei, sans-serif;
}

.layout-footer {
    background-color: #eee;
}

.divider {
    margin: 15px 0 !important;
    background: #eee !important;
}
</style>
<template>
    <div class="layout-base">
        <Layout>

            <div style="padding-left: 15px; padding-bottom: 20px; background-color: #fff;">
                <Header class="layout-header">
                    <Row>
                        <Col>
                        <h1 style="font-size: 36px;height: 30px;font-weight: 800; font-style: italic;">蓝鱼的博客 </h1>
                        </Col>
                    </Row>
                    <div
                        style="font-size: 15px;height: 10px; float: left; font-style: italic;color: #999; margin-top: 5px;">
                        学要学的踏实，玩要玩的痛快
                    </div>

                </Header>
                <div><img style="width:100%; height: 100%;" src="../assets/testbg2.png"></div>
            </div>


            <Layout class="layout-center">
                <Content class="layout-content">
                    <div>

                        <Card dis-hover :bordered="false" style="width:100%;border-radius:0px;margin-bottom: 20px;"
                            v-for='index in 1' :key='index'>
                            <div style="text-align:left">
                                <!-- <img src="https://dev-file.iviewui.com/stJXDnKhL5qEBD0dHSDDTKbdnptK6mV5/large"> -->
                                <div style="font-size:28px;font-weight: 600;"><a style="color: #000;">个人博客搭建指南</a></div>
                                <div style="color: #666; margin-top:10px; font-size: 16px;">
                                    <a style="color: #333;">简单介绍个人博客搭建过程，所用到的前端技术和后端服务，目前技术方案是： 
                                        VUE为前端交互技术栈，SprinBoot+MySQL作为后台业务技术栈，后期会创建博客后台管理系统……</a>
                                    <!-- <span style="margin-left: 10px;"><Button size="small" type="default">阅读全文</Button></span> -->
                                </div>
                                <div style="color: #999; margin-top:10px; font-size: 8px;">
                                    <span>2023年3月18日 · vue · <a style="border-radius:50%;color:#999;">博客</a> </span>
                                </div>
                            </div>
                        </Card>

                    </div>

                </Content>
                <Sider class="layout-sider" hide-trigger>
                    <div style="margin-left: 50px; margin-top: 50px;">
                        <Row>
                            <Col>
                            <div style="float: left;  font-size: 16px;font-weight: bold;color: #6e7173;">分类</div>
                            </Col>
                        </Row>

                        <Divider class="divider" />

                        <Row>
                            <Col>
                            <div style="margin: 8px; margin-left: 2px;" v-for='index in 1' :key='index'><a
                                    style="color: #6e7173; font-size: 15px;">Vue（1）</a></div>

                            </Col>
                        </Row>

                        <Divider class="divider" />

                        <Row>
                            <Col>


                            <Button label="small" v-for='index in 1' :key='index'
                                style="float: left; margin: 3px; padding: 5px;">VUE</Button>

                            </Col>
                        </Row>

                    </div>
                </Sider>
            </Layout>
            <!-- <Divider class="divider" /> -->
            <Footer class="layout-footer">© 2023 蓝鱼的博客 By 蓝鱼 | <a style="color:#666;" href="https://beian.miit.gov.cn">粤ICP备2023011988号-1</a></Footer>
        </Layout>


    </div>
</template>
<script>
import { Button } from 'view-ui-plus';


export default {
    components: { Button }
}
</script>
