# demo-open-mobile-network-platform-project

SDN-based Control and Management Architecture for Heterogeneous Cognitive Networks
(Appendix)

Appendix A
$ sudo pip3 install tornado sqlalchemy construct==2.5.2 protobuf protobuf3-to-dict
At the Agent:
$ wget https://github.com/protobuf-c/protobuf-c/releases/download/v1.2.1/protobuf-c-1.2.1.tar.gz
$ tar xvfz protobuf-c-1.2.1.tar.gz
$ cd protobuf-c-1.2.
$./configure
$ Make
$ sudo make install
For exchanging data, we customized the data description file (main.proto) for parsing data, where the message is defined as follows:
message header {
       required uint32 vers = 1;
       required uint32 b_id = 2;
       required uint32 seq = 3;
       required uint32 t_id = 4;
        required double mUA=5;
       required double mPA=6;
       required double GRB1=7;
       required double GRB2=8;
       required double GRB3=9;
       required double GRB4=10;
       required double GRB5=11;
        required double td1=12; 
        required double td2=13; 
        required double td3=14; 
        required double td4=15; 
        required double td5=16; 
        required double td6=17; 
        required double td7=18; 
        required double td8=19; 
        required double td9=20; 
        required double td10=21;
        required double td11=22;
        required double td12=23;
        required double td13=24;
        required double td14=25;
        required double td15=26;
        required double td16=27;
        required double td17=28;
        required double td18=29;
        required double td19=30;
        required double td20=31;
}
where .proto file is converted to C  files (main.pb-c.c, main.pb-c.h) at the agent side through the use of the following commands:
$./ cd empower-eNB-agent/proto
$./make
$./sudo make install
$./cd ../agent
$./make
$./sudo make install
where the message is defined as follows:
static const ProtobufCFieldDescriptor header__field_descriptors[31] =
{
  {
    "vers",
    1,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_UINT32,
    0,   /* quantifier_offset */
    offsetof(Header, vers),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "b_id",
    2,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_UINT32,
    0,   /* quantifier_offset */
    offsetof(Header, b_id),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "seq",
    3,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_UINT32,
    0,   /* quantifier_offset */
    offsetof(Header, seq),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "t_id",
    4,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_UINT32,
    0,   /* quantifier_offset */
    offsetof(Header, t_id),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "mUA",
    5,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_DOUBLE,
    0,   /* quantifier_offset */
    offsetof(Header, mua),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "mPA",
    6,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_DOUBLE,
    0,   /* quantifier_offset */
    offsetof(Header, mpa),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "GRB1",
    7,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_DOUBLE,
    0,   /* quantifier_offset */
    offsetof(Header, grb1),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "GRB2",
    8,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_DOUBLE,
    0,   /* quantifier_offset */
    offsetof(Header, grb2),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "GRB3",
    9,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_DOUBLE,
    0,   /* quantifier_offset */
    offsetof(Header, grb3),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },
  {
    "GRB4",
    10,
    PROTOBUF_C_LABEL_REQUIRED,
    PROTOBUF_C_TYPE_DOUBLE,
    0,   /* quantifier_offset */
    offsetof(Header, grb4),
    NULL,
    NULL,
    0,             /* flags */
    0,NULL,NULL    /* reserved1,reserved2, etc */
  },


Appendex B
$ protoc --proto_path=proto --python_out=empower/vbsp/messages proto/main.proto 
where the message is described as follows:
_HEADER = _descriptor.Descriptor(
  name='header',
  full_name='header',
  filename=None,
  file=DESCRIPTOR,
  containing_type=None,
  fields=[
    _descriptor.FieldDescriptor(
      name='vers', full_name='header.vers', index=0,
      number=1, type=13, cpp_type=3, label=2,
      has_default_value=False, default_value=0,
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='b_id', full_name='header.b_id', index=1,
      number=2, type=13, cpp_type=3, label=2,
      has_default_value=False, default_value=0,
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='seq', full_name='header.seq', index=2,
      number=3, type=13, cpp_type=3, label=2,
      has_default_value=False, default_value=0,
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='t_id', full_name='header.t_id', index=3,
      number=4, type=13, cpp_type=3, label=2,
      has_default_value=False, default_value=0,
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='mUA', full_name='header.mUA', index=4,
      number=5, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='mPA', full_name='header.mPA', index=5,
      number=6, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='GRB1', full_name='header.GRB1', index=6,
      number=7, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='GRB2', full_name='header.GRB2', index=7,
      number=8, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='GRB3', full_name='header.GRB3', index=8,
      number=9, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='GRB4', full_name='header.GRB4', index=9,
      number=10, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='GRB5', full_name='header.GRB5', index=10,
      number=11, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td1', full_name='header.td1', index=11,
      number=12, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td2', full_name='header.td2', index=12,
      number=13, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td3', full_name='header.td3', index=13,
      number=14, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td4', full_name='header.td4', index=14,
      number=15, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td5', full_name='header.td5', index=15,
      number=16, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td6', full_name='header.td6', index=16,
      number=17, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td7', full_name='header.td7', index=17,
      number=18, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td8', full_name='header.td8', index=18,
      number=19, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td9', full_name='header.td9', index=19,
      number=20, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td10', full_name='header.td10', index=20,
      number=21, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td11', full_name='header.td11', index=21,
      number=22, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td12', full_name='header.td12', index=22,
      number=23, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td13', full_name='header.td13', index=23,
      number=24, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td14', full_name='header.td14', index=24,
      number=25, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td15', full_name='header.td15', index=25,
      number=26, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td16', full_name='header.td16', index=26,
      number=27, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td17', full_name='header.td17', index=27,
      number=28, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td18', full_name='header.td18', index=28,
      number=29, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td19', full_name='header.td19', index=29,
      number=30, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
    _descriptor.FieldDescriptor(
      name='td20', full_name='header.td20', index=30,
      number=31, type=1, cpp_type=5, label=2,
      has_default_value=False, default_value=float(0),
      message_type=None, enum_type=None, containing_type=None,
      is_extension=False, extension_scope=None,
      options=None),
  ],














Appendix C
lte-softmodem.c
-----------------------------------------------------------------------------------------------------------------
#ifdef EMAGE_AGENT
// Only one module is supported in OAI i.e (mod_id 0)
spectrum_sensing_grb5 = atof(sSSR5);//511011; // will get from sensing function
//// end of code///
// made by Mr. Aselme --> tested
double p_ue_rx1 = 1086004400210; // dowlink transmit power or Tx_gain
double p_ue_rx2 = 1086004400220; // dowlink transmit power or Tx_gain
double p_ue_rx3 = 1175017501750; // dowlink transmit power or Tx_gain 175: NO ue
double p_ue_rx4 = 1175017501750; // dowlink transmit power or Tx_gain
double p_ue_rx5 = 1175017501750; // dowlink transmit power or Tx_gain

double rsvp1 = vRSRP1// 1075007600770; // dowlink transmit power or Tx_gain 075: -75 dBm
double rsvp2 = 1079007200750; // dowlink transmit power or Tx_gain
double rsvp3 = 1175017501750; // dowlink transmit power or Tx_gain // NO ue
double rsvp4 = 1175017501750; // dowlink transmit power or Tx_gain // NO ue
double rsvp5 = 1175017501750; // dowlink transmit power or Tx_gain // nO ue

double spectrum_sensing_grb1 = 101011; // will get from sensing function
double spectrum_sensing_grb2 = 201011; // will get from sensing function
double spectrum_sensing_grb3 = 311011; // will get from sensing function
double spectrum_sensing_grb4 = 401101; // will get from sensing function
double spectrum_sensing_grb5 = 511011; // will get from sensing function

double td1=spectrum_sensing_grb1;
double td2=spectrum_sensing_grb2;
double td3=spectrum_sensing_grb3;
double td4=spectrum_sensing_grb4;
double td5=spectrum_sensing_grb5;
double td6=spectrum_sensing_grb5;

double td7=p_ue_rx1;
double td8=p_ue_rx2;
double td9=p_ue_rx3;
double td10=p_ue_rx4;
double td11=p_ue_rx5;

double td12=rsrp1;
double td13=rsrp2;
double td14=rsrp3;
double td15=rsrp4;
double td16=rsrp5;

double td17=0;
double td18=0;
double td19=0;
double td20=0;


//receiving from controller
double mua=1.0;
double mpa=2.5;
double grb1=58.0;
double grb2=58.0;
double grb3=58.0;
double grb4=45.5;
double grb5=12.0;

//end of code
printf("Check for eNB-4");
em_start(&sim_ops, enb_properties->properties[0]->eNB_id,mua, mpa, grb1, grb2,grb3,grb4,grb5, td1, td2, td3, td4, td5, td6, td7, td8, td9, td10, td11, td12, td13, td14, td15, td16, td17, td18, td19, td20);
printf("Check for eNB-3");
#endif /* EMAGE_AGENT */




Appendix D
from __future__ import division
"""
Created on Wed May 11 13:10:20 2017
Translated from matlab files Dr. ThanzinOo
@author: LE ANH TUAN
"""
#===============================================================================
from numpy import int
import numpy as np
from scipy.spatial.distance import cdist
import random
from empower.vbsp.project_modules import *
from cvxpy import error
import sys
#===============================================================================
#clear_all.clear_all()
#===============================================================================
# class Controller_Name:
#     nBS = 0;  # Number of BSs
#     nMBS = 0; # Number of MBSs
#     nPBS = 0; # Number of PBSs
#     nFBS = 0; # Number of GBSs
#
#     nRB = 0;  # Number of resource blocks
#
#     nUE = 0;  # Number of UEs
#
#     mUA = []; # User association matrix
#     mFUA = []; # User association matrix
#     mRBA = [];# Resource blocks allocation matrix
#
#     rMBS = 0; # Radius of MBS
#     rPBS = 0; # Radius of PBS
#     rFBS = 0; # Radius of FBS
#
#     pBS  = [];# Transmit power of all BSs
#     pMBS = 0; # Radius of MBS
#     pPBS = 0; # Radius of PBS
#     pFBS = 0; # Radius of FBS
#
#     cBS = []; # Coor of MBS
#     cMBS =[];# Coor of MBS
#     cPBS =[];# Coor of PBS
#     cFBS =[];# Coor of FBS
#
#     cUE = []; # Coor of FBS
#
#     RefPL = [];# nBSx1
#
#     BS_Dist = []; # nBS x nBS: distance among BSs
#
#     FFT_size = 0;
#
#     def __init__(self, name): # project name
#         self.name = name
#     def info(self,Controller_Name):
#         print('nBS= {0}, nUE= {1}, nRB:= {2}'.format(Controller_Name.nBS,
#               Controller_Name.nRB,Controller_Name.nUE))
#         return 0
#
# class BS_Types(object):
#     """__init__() functions as the class constructor"""
#     def __init__(self, Type='None', TxPower_sCH=[], TxHeight=0,TxGain = 0,
#                  CellRadius = 0, RefPL = 0, TotalPower = 0):
#         self.Type = Type
#         self.TxPower_sCH = TxPower_sCH;   # Per sub-channel Transmit Power [watt]
#         self.TxHeight = TxHeight; # Transmit antenna height [metre]
#         self.TxGain = TxGain; # Transmit antenna gain [dBi]
#         self.CellRadius = CellRadius; # Cell radius of BS [metre]
#         self.RefPL = RefPL; # Reference path loss [dBm]
#         self.TotalPower = TotalPower;
#
# class User_Equipment(object):
#     """__init__() user equipment class"""
#     def __init__(self, name='None', BS=None, P_Tx=None,RB = None, Rate = None,
#                  Power = None,pExp = None,Explored = None, Utility = None):
#         self.name = name
#         self.BS = BS
#         self.P_Tx = P_Tx
#         self.RB = RB
#         self.Rate = Rate
#         self.Power = Power
#         self.pExp = pExp
#         self.Explored = Explored
#         self.Utility = Utility
#
# class Base_Station(object):
#     """__init__() base station class"""
#     def __init__(self, name='None', cell_radius = 0, user_association=0,
#                  transmit_power=0,uplink_RB_allocation = [],
#                  downlink_RB_allocation = [],cell_location = [],RefRP = 0,TxPower_RB=[]):
#         self.name = name
#         self.user_association = user_association
#         self.transmit_power = transmit_power
#         self.uplink_RB_allocation = uplink_RB_allocation
#         self.downlink_RB_allocation = downlink_RB_allocation
#         self.cell_location = cell_location
#         self.cell_radius = cell_radius
#         self.RefRP = RefRP
#         self.TxPower_RB = TxPower_RB

#===============================================================================
def scheduling_algoirthm(M1,M2,M3,M4,M5,M6,M7):
    MNO = Controller_Name('----Project Name: Markov approximation-based learning in 5G network---')
    ###### ----> INPUT PARAMETERs
    print ('Updating network parameter from eNB and UE to SDN controller...')
    # Network size
    MNO.nBS = 3;            # Number of BSs
    MNO.nFBS = 3;           # Number of FBSs
    MNO.nUE = 5;            # Number of UEs
    MNO.nRB = 25;           # Number of RBs
    MNO.nTotCar = 300;       # Total number of subcarriers = 25 RB
    nHistory = 100
    print ('Initializing Algorithm parameters')
    nIterations = 80
    beta_step = 8
    conv_stop = 50
    Algorithm = 3 # MCDA = 1; PLLA = 2; SOA = 3;
    if Algorithm ==1: # MCDA
        pExp = 1
        pEstep = 0
        Str2 =  'OP_MA_' + str(MNO.nUE) + '.mat'
    if Algorithm == 2: # PLLA
            pExp = 0.5
            pEstep = 0
            Str2 =  'OP_LL_' + str(MNO.nUE) + '.mat'
    if Algorithm == 3: # SOA
            pExp = 1
            pEstep = 0.1
            Str2 =  'OP_SOA_' + str(MNO.nUE) + '.mat'
    # initialization matrix to update: 
    print ('Initializing output parameters to the MNO...')
    MNO.P_Tx_UExBS_RB = np.zeros(shape=(MNO.nUE,MNO.nBS),dtype = float)
    MNO.Rate_UExBS_RB = np.zeros(shape=(MNO.nUE,MNO.nBS),dtype = float)  
    MNO.Intf_UExBS_RB= np.zeros(shape=(MNO.nUE,MNO.nBS),dtype = float)  
    MNO.mnRBA = np.zeros(shape=(MNO.nUE,MNO.nBS))  
    MNO.SINR_UE_BS_RB = np.zeros(shape=(MNO.nUE,MNO.nBS),dtype = float)  
    MNO.mUA = np.zeros(shape=(MNO.nUE,MNO.nBS), dtype = int) #
    MNO.mRBA = np.zeros(shape=(MNO.nRB,MNO.nBS),dtype=bool) # resource allocation 
    MNO.OP_Rate = np.zeros(shape=(MNO.nUE,MNO.nBS),dtype = float)
    MNO.OP_Cost = np.zeros(shape=(MNO.nUE,MNO.nBS),dtype = float)
    MNO.OP2_User = np.zeros(shape=(nIterations,MNO.nBS),dtype = int)
    MNO.OP2_User = np.zeros(shape=(nIterations,MNO.nBS),dtype = float)
    MNO.OP2_Cost = np.zeros(shape=(nIterations,MNO.nBS),dtype = float)
    MNO.BS_Cmap = np.zeros(shape=(MNO.nBS,MNO.nBS),dtype = float)
    MNO.BS_Rmap = np.zeros(shape=(MNO.nBS,MNO.nBS),dtype = float)
    P = np.zeros(shape=(MNO.nRB,MNO.nBS)) # Control variable for power
    U = np.zeros(shape=(MNO.nUE,MNO.nBS)) # Utility --> Revenue - Cost
    pExpVec = np.ones(MNO.nUE,dtype = float)
    #===============================================================================
    #===============================================================================
    print ('Getting Device information from testbed system')
    
    BS_list = ["3618","3619","3620"] # via BS id set at configuration file
    UE_list = ["UE-id-1","UE-id-2","UE-id-3","UE-id-4","UE-id-5"] # via UE emei
    tx_gain_bs = M1#[89.75,89.75,89.75] # via BS id set at configuration file 
    rx_gain_ue = M2 #[21,21,21,21,21] # via UE emei
    
    print ('Conflict and Resue Graphs for Base Stations ... ') # where??? 
    
    MNO.BS_Cmap = M3#np.array([[0, 0, 1], 
#                            [0, 0, 1],
 #                           [1, 1, 0]])
    
    MNO.BS_Rmap = M4 #np.array([[1, 0, 0],
  #                          [0, 1, 0],
   #                         [0, 0,  1]])
    
    MNO.P_Rx =  M5 #np.array([[-69.12372078, -74.1376763,  -71.82325875],
    #                      [-53.83030764, -70.29361338, -74.97618152],
     #                     [-59.74909419, -67.796359,   -75.62515563],
      #                    [-66.54979872, -74.95372667, -69.25830752],
       #                   [-61.29133112, -73.60238591, -70.5957919 ]])
    #===============================================================================
    # print 'Getting SINR level'
    # MNO.P_Rx = 10**(0.1*MNO.P_Rx)
    # #print 'MNO.P_Rx', MNO.P_Rx
    # for k1 in range(MNO.nUE):
    #     for k2 in range(MNO.nBS):
    #         MNO.Intf_UExBS_RB[[k1],[k2]] = np.dot(MNO.P_Rx[[k1],:], MNO.BS_Rmap[:,[k2]]) # Wats            
    #         MNO.SINR_UE_BS_RB[[k1],[k2]] = MNO.P_Rx[[k1],[k2]] / (MNO.Intf_UExBS_RB[[k1],[k2]]  + MNO.N0) # Wats
    #         
    # SINR_dB = 10*np.log10(MNO.SINR_UE_BS_RB)
    MNO.Intf_UExBS_RB = M6 # np.array([[  6.57164546e-08,   6.57164546e-08,   1.60925213e-07],
    #                               [  3.17966852e-08,   3.17966852e-08,   4.23316627e-06],
     #                              [  2.73832150e-08,  2.73832150e-08,   1.22557256e-06],
      #                             [  1.18623094e-07,   1.18623094e-07,   2.53281241e-07],
       #                            [  8.71807921e-08,   8.71807921e-08,   7.86419045e-07]])
    SINR_dB = M7 # np.array([[  2.69953797, -2.31441755,  -3.88949969],
        #                [ 21.14587388,   4.68256814, -21.24283479],
         #               [ 15.87606144,   7.82879663, -16.50854592],
          #              [  2.7085088,   -5.69541915,  -3.29433778],
           #             [  9.30446078,  -3.00659401,  -9.55233212]])
    MNO.pFBS = 30;             # Power of FBSs
    Noise = calculateNoise.calculateNoise(5)  # [dBm] Thermal noise floor with BW = 5MHz.
    MNO.N0 = 10**((Noise-30)/10) # [W]
    #===============================================================================
    MNO.UE_DL_Demand = np.array([ 1650000,  1350000,  1200000,  1500000,  1350000])      
    #===============================================================================
    #=========Initialization classes
    print ('Initializing BSs and UEs')
    # base station
    base_station = []
    i = 0  
    for i in range(MNO.nBS):              
        base_station.append(Base_Station('FBS-id:= fbs-'+str(i),MNO.rFBS,[],MNO.pFBS,[], [], [],0,MNO.pFBS))            
    # user  
    UE = [] 
    for i in range(MNO.nUE):       
        UE.append(User_Equipment('UE-id:= ue-'+str(i),[],[],[],[],[],[],[],[]))
    #===============================================================================
    # === --> Compute RBs for each virutal UE given the UE demand
    MNO.mFUA = (SINR_dB >= -12) # 9 dBm is interference threshold
    for k1 in range(MNO.nUE):
        for k2 in range(MNO.nBS):
            if MNO.mFUA[[k1],[k2]] == 1:
                # Calculate Achievable rate per unit RB
                MNO.Rate_UExBS_RB[[k1],[k2]] = calculateMaxThroughputOfTheNode.calculateMaxThroughputOfTheNode(SINR_dB[[k1],[k2]],100,50)
                # Calculate # of RB to meet UE demand
                MNO.mnRBA[[k1],[k2]] = np.ceil(MNO.UE_DL_Demand[k1]/MNO.Rate_UExBS_RB[[k1],[k2]])  # we will execute this one  
    for k1 in range(MNO.nUE):    
        UE[k1].BS = np.zeros(nHistory, dtype = int)
        UE[k1].P_Tx = np.zeros(nHistory, dtype = float)        
        UE[k1].RB = np.zeros(shape=(MNO.nRB,nHistory),dtype = bool)
        UE[k1].Rate = np.zeros(nHistory, dtype = float)
        UE[k1].Power = np.zeros(nHistory, dtype = float)  
        UE[k1].Utility = np.zeros(nHistory, dtype = float)
        UE[k1].beta = 0
        UE[k1].Explored = 0
    ##### --> UA allocation between virutal BSs and virtual UEs
    for k1 in range(MNO.nUE):     
        SINR_max = np.amax(SINR_dB[[k1],:]) # Maximum SINR UE association --> will create an array[ [0,0,0], [1, 3, 5]] for ex.
        BS_ind1 = np.where(SINR_dB[[k1],:]==SINR_max) # Maximum SINR UE association        
        BS_ind = BS_ind1[1][0]       
        MNO.mUA[[k1],[BS_ind]] = 1    # cell association   
    ##### ---> RBs allocation to virtual UEs        
        BS_Conflict = MNO.BS_Cmap[[BS_ind],:] # Conflict BS of BS_ind    
        print (BS_Conflict[0])
        BS_Conflict_id = []
        BS_Conflict_id = []
        for k2 in range(MNO.nBS):
            if BS_Conflict[0][k2] == 1:
                if not BS_Conflict_id: 
                    BS_Conflict_id = np.array([k2])
                else:
                    BS_Conflict_id = np.concatenate((BS_Conflict_id,[k2]),axis=1)            
        tmp1 = np.sum(MNO.mRBA[:,BS_Conflict_id],axis=1) # check again when you have a results. axist = 0 or 1
        tmp11 = np.where(tmp1==0) # find the number of available RBs
        tmp11 = tmp11[0] # get the first array in finding results
        if len(tmp11)>=MNO.mnRBA[[k1],[BS_ind]]:                
            temp111 = MNO.mnRBA[[k1],[BS_ind]]
            temp111 = temp111[0] # because   MNO.mRBA[[k1],[BS_ind]] is an array    
            temp111 = temp111.astype(int) 
            tmp2 = tmp11[0:temp111] # allocate availes RBs to the UE k1
        else: 
            print ('Error: the system is not enought RBs to allocate for this UE!'        )
            sys.exit(1)        
                
        MNO.mRBA[tmp2, [BS_ind]] = 1 # Fill up the used RBs.           
    #### ---> UPdate to virtual UE at the controller    
        UE[k1].BS[-1] = BS_ind  # update cell at UE side        
        UE[k1].P_Tx[-1] = MNO.P_Tx_UExBS_RB[[k1],[BS_ind]] # update transmit power downlink
        UE[k1].RB[np.transpose(tmp2),[-1]] = MNO.mRBA[np.transpose(tmp2), [BS_ind]] # update RBs to UE    
        UE[k1].Rate[-1] = MNO.mnRBA[[k1],[BS_ind]] * MNO.Rate_UExBS_RB[[k1],[BS_ind]] #    
        UE[k1].Power[-1] = MNO.mnRBA[[k1],[BS_ind]] * MNO.P_Tx_UExBS_RB[[k1],[BS_ind]] # Total power     
        UE[k1].Utility[-1] = UE[k1].Rate[-1] - UE[k1].Power[-1]*10000 # cost = 0.1     
        MNO.mUA[[k1],[BS_ind]] = 1 #    
    # ---> Learning ================================================
    print('\n Starting log linear learning algorithm...\n')
    for t in range(nIterations):
        print ('Epoch number:', t , '\n'     )
        print ('Updating paramerters to learn...'      )
        #===========================================================================
        # Do we need update these value when we run the algorithm
        # # Calculate SINR --> this one is recomputed from above
        # MNO.SINR_UE_BS_RB[:] = 0 # reset
        # for k1 in range(MNO.nUE):
        #     for k2 in range(MNO.nBS):
        #         MNO.Intf_UExBS_RB[[k1],[k2]] = np.dot(MNO.P_Rx[[k1],:], MNO.BS_Rmap[:,[k2]]) # Wats            
        #         MNO.SINR_UE_BS_RB[[k1],[k2]] = MNO.P_Rx[[k1],[k2]] / (MNO.Intf_UExBS_RB[[k1],[k2]]  + MNO.N0) # Wats    
        # SINR_dB = 10 * np.log10(MNO.SINR_UE_BS_RB)     
        # MNO.mFUA = (SINR_dB >= -12) # X is variable for association --> true or false valuas    
        # MNO.mnRBA = np.zeros(shape=(MNO.nUE,MNO.nBS))     
        # for k1 in range(MNO.nUE):
        #     for k2 in range(MNO.nBS):
        #         if MNO.mFUA[[k1],[k2]] == 1:
        #             # Calculate Achievable rate per unit RB
        #             MNO.Rate_UExBS_RB[[k1],[k2]] = calculateMaxThroughputOfTheNode.calculateMaxThroughputOfTheNode(SINR_dB[[k1],[k2]],Dist[[k1],[k2]],MNO.rFBS)   # we will execute this one 
        #             # Calculate # of RB to meet UE demand
        #             MNO.mnRBA[[k1],[k2]] = np.ceil(MNO.UE_DL_Demand[k1]/MNO.Rate_UExBS_RB[[k1],[k2]])  # we will execute this one  
        #             
        #===========================================================================
        UE_list = np.random.permutation(MNO.nUE) 
        UE_list = np.array(UE_list) # randomly choose UE index to process
        
        print ('Learning user association... \n')
        for k1 in range(MNO.nUE): 
            k2 = UE_list[k1]   # UE to process
            F_v = np.where(MNO.mFUA[[k2],:]==1) # which BSs are can be connected ?                      
            f_t = UE[k2].BS # list of BSs was connected 
            u_t = UE[k2].Utility # list of Utility was connected 
            iExp = UE[k2].Explored # exploration probability 
            pExp = pExpVec[k2]     # exploration probability 
            beta = UE[k2].beta     #                        
            F_v = F_v[1].astype(int)        
            f_t, u_t, iExp = fun_SelfOrganize.fun_SelfOrganize(F_v,f_t,u_t, iExp,pExp,beta) # each UE                         
            if len(F_v) == 1: 
                pExp = 0                        
            UE[k2].BS = f_t 
            UE[k2].Explored = iExp
            pExpVec[k2] = pExp
            
        print ('Learning resource allocation...')
     
        MNO.mUA[:] = 0
        MNO.mRBA[:] = 0 # why we need delete all database at the controller? we have to reallocte all 
        for k1 in range(MNO.nUE):        
            k2 = UE_list[k1]  # UE index to process       
            BS_ind = UE[k2].BS[[-1]] #         
            BS_ind = BS_ind[0] #BS_ind = 4                
            MNO.mUA[[k2],UE[k2].BS[-1]] = 1 # Associating BS        
            BS_Conflict = MNO.BS_Cmap[[BS_ind],:] # Conflict BS of BS_ind        
            
            #print BS_Conflict[0]
            BS_Conflict_id = []
            BS_Conflict_id = []
            for k3 in range(MNO.nBS):
                if BS_Conflict[0][k3] == 1:
                    if not BS_Conflict_id: 
                        BS_Conflict_id = np.array([k3])
                    else:
                        BS_Conflict_id = np.concatenate((BS_Conflict_id,[k3]),axis=1)        
                        
            tmp1 = np.sum(MNO.mRBA[:,BS_Conflict_id],axis=1) # check again when you have a results. axist = 0 or 1
            tmp11 = np.where(tmp1==0) # find the number of available RBs
            tmp11 = tmp11[0] # get the first array in finding results
            if len(tmp11)>=MNO.mnRBA[[k1],[BS_ind]]:                
                temp111 = MNO.mnRBA[[k1],[BS_ind]]
                temp111 = temp111[0] # because   MNO.mRBA[[k1],[BS_ind]] is an array
                temp111 = temp111.astype(int)     
                tmp2 = tmp11[0:temp111] # allocate availes RBs to the UE k1
            else: 
                print ('Error: the system is not enought RBs to allocate for this UE!'            )
                sys.exit(1)        
    
            MNO.mRBA[tmp2, [BS_ind]] = 1 # Fill up the used RBs.        
    
            print ('Updating data to Virtual UEs ...')
                    
            UE[k2].BS[-1] = BS_ind  # update cell at UE side        
            UE[k2].P_Tx[-1] = MNO.P_Tx_UExBS_RB[[k2],[BS_ind]] # update transmit power downlink
            UE[k2].RB[np.transpose(tmp2),[-1]] = MNO.mRBA[np.transpose(tmp2), [BS_ind]] # updating RBs to UE         
            UE[k2].Rate[-1] = MNO.mnRBA[[k2],[BS_ind]] * MNO.Rate_UExBS_RB[[k2],[BS_ind]] #        
            UE[k2].Power[-1] = MNO.mnRBA[[k2],[BS_ind]] * MNO.P_Tx_UExBS_RB[[k2],[BS_ind]] # Total power         
            UE[k2].Utility[-1] = UE[k2].Rate[-1] - UE[k2].Power[-1]*100 # cost = 0.1         
            MNO.mUA[[k2],[BS_ind]] = 1 #           
                   
            print ('Updating parameter in the learning algorithm ...')
            if np.isnan(UE[k2].Rate[-1]):
                break
            if UE[k2].Utility[-1] >= UE[k2].Utility[-2]:
                UE[k2].beta = UE[k2].beta + beta_step
                pExpVec[k2] = np.max([0, pExpVec[k2]-pEstep])
                                
            tmp1 = UE[k2].BS[-1]        
            MNO.mUA[k2] = tmp1
            MNO.OP_Rate[[k2],[tmp1]] = UE[k2].Rate[-1]
            MNO.OP_Cost[[k2],[tmp1]] = UE[k2].Power[-1]
                
        print ('Exporting output results ')
        MNO.OP2_User[[t],:] = np.transpose(np.sum(MNO.mUA))
        MNO.OP2_User[[t],:] = np.transpose(np.sum(MNO.OP_Rate * MNO.mUA))    
        MNO.OP2_Cost[[t],:] = np.transpose(np.sum(MNO.OP_Cost * MNO.mUA))        
        #===========================================================================
        # Total_pExplore = 0    
        # for k1 in range(MNO.nUE):
        #     Total_pExplore = Total_pExplore + pExpVec[k1]
        # if Total_pExplore == 0:
        #     break
        #===========================================================================
    
    print ('Output: sending our proposals to eNBs and UEs!')
    
    print ('Waiting estimation total utility!')
    
    print ('Mission completed! Goodluck!')
    
    #===============================================================================
    print ('Display information ...')
#    DisplayNetwork.DisplaymRBA_RB_BS(MNO.mRBA, MNO.nRB, MNO.nBS)
#    DisplayNetwork.DisplaymUE1Utility(UE[1].Utility)
    print ('UE[1].Utility=',UE[1].Utility)
    
    return UE[1].Utility
#==============================================================================
# End of algorithm     
#==============================================================================

#==============================================================================
# # testing 
MNO = Controller_Name('----Project Name: Markov approximation-based learning in 5G network---')
#==============================================================================
M1 = [89.75,89.75,89.75] # via BS id set at configuration file
M2 = [21,21,21,21,21] # via UE emei

M3 = np.array([[0, 0, 1],
               [0, 0, 1],
                [1, 1, 0]])

M4 = np.array([[1, 0, 0],
               [0, 1, 0],
                [0, 0,  1]])

M5 =  np.array([[-69.12372078, -74.1376763,  -71.82325875],
                          [-53.83030764, -70.29361338, -74.97618152],
                          [-59.74909419, -67.796359,   -75.62515563],
                          [-66.54979872, -74.95372667, -69.25830752],
                          [-61.29133112, -73.60238591, -70.5957919 ]])
    #===============================================================================
    # print 'Getting SINR level'
    # MNO.P_Rx = 10**(0.1*MNO.P_Rx)
    # #print 'MNO.P_Rx', MNO.P_Rx
    # for k1 in range(MNO.nUE):
    #     for k2 in range(MNO.nBS):
    #         MNO.Intf_UExBS_RB[[k1],[k2]] = np.dot(MNO.P_Rx[[k1],:], MNO.BS_Rmap[:,[k2]]) # Wats
    #         MNO.SINR_UE_BS_RB[[k1],[k2]] = MNO.P_Rx[[k1],[k2]] / (MNO.Intf_UExBS_RB[[k1],[k2]]  + MNO.N0) # Wats
    #
    # SINR_dB = 10*np.log10(MNO.SINR_UE_BS_RB)
M6 =MNO.Intf_UExBS_RB =  np.array([[  6.57164546e-08,   6.57164546e-08,   1.60925213e-07],
                                   [  3.17966852e-08,   3.17966852e-08,   4.23316627e-06],
                                   [  2.73832150e-08,  2.73832150e-08,   1.22557256e-06],
                                   [  1.18623094e-07,   1.18623094e-07,   2.53281241e-07],
                                   [  8.71807921e-08,   8.71807921e-08,   7.86419045e-07]])
M7 = SINR_dB = np.array([[  2.69953797, -2.31441755,  -3.88949969],
                        [ 21.14587388,   4.68256814, -21.24283479],
                        [ 15.87606144,   7.82879663, -16.50854592],
                        [  2.7085088,   -5.69541915,  -3.29433778],
                        [  9.30446078,  -3.00659401,  -9.55233212]])
result = scheduling_algoirthm(M1,M2,M3,M4,M5,M6,M7)












Appendix E
from __future__ import division
import numpy as np 
import empower.vbsp.project_modules.fun_ChooseProb
import empower.vbsp.project_modules.fun_Sigmoid
def fun_SelfOrganize(F_v, f_t, u_t, iExp, pExp, beta):
    '''
    % fun_SelfOrganize performs the self organization via learning and
    % consolidation.
    % First, learning stage randomly chooses a possible configuration.
    % Second, consolidation stage compares the new result with old results
    % and choose the higher payoff configuration with higher probability.
    %
    % Inputs:   F_v     - Vector of all feasible configurations
    %           U_v     - Utility corresonding to all feasible configurations
    %           f_t     - Historical vector of chosen configurations
    %           u_t     - Historical utilities of chosen configurations
    %           iExp    - Indicator showing Explored (1) / Unexplored (0)
    %                     status at previous timeslot
    %           pExp    - Exploration probability (learning rate)
    %           beta    - Annealing factor
    %
    % Outputs:  Same as Inputs
    '''    
    old_f_t = f_t[1:(len(f_t))]
    f_t[0:(len(f_t)-1)] = old_f_t # update configuratin history; len(f_t) = 1:end-1 in matlab
    old_u_t = u_t[1:(len(u_t))]
    u_t[0:(len(u_t)-1)] = old_u_t # update configuratin history; len(f_t) = 1:end-1 in matlab 
    
    if iExp == 0: # Learning        
        Exp = empower.vbsp.project_modules.fun_ChooseProb.fun_ChooseProb(np.array([pExp, 1-pExp]), np.array([1, 2])) # ?????
        F_v = list(F_v)                   
        temp = list([f_t[-2]])
        #print 'temp', temp
        #print 'F_v', F_v             
        if Exp == 1: # Exploration --> Choose a new configuration randomly                    
            Utility_0 = list(set(F_v)-set(temp))# setdiff(F_v,f_t(end-1)) # ???                       
            if not Utility_0:                
                f_t[-1] = f_t[-2]                
            else:
                #print 'ok2' 
                nChoice = len(Utility_0)
                Prob0 = 1/nChoice * np.ones(shape=(nChoice,1)) # calculate uniform probability                
                choice = empower.vbsp.project_modules.fun_ChooseProb.fun_ChooseProb(Prob0, np.arange(nChoice)) # ??? testing ????
                # print ('choice', choice)
                choice = choice[0]   
                f_t[-1] = Utility_0[choice] 
                #print 'Utility_0=',Utility_0,'choice=',choice  
                #print 'f_t[-1]=', f_t              
                #print f_t[10000]           
            iExp = 1                   
        else: # Exploitation --> Stay with the previous configuration
            f_t[-1]= f_t[-2]
            #print 'ok3' 
    else: # Consolidation        
        Utility_1 = u_t[-3] - u_t[-2]
        nu = empower.vbsp.project_modules.fun_Sigmoid.fun_Sigmoid(beta, Utility_1) # fun_Sigmoid
        #print ('nu=', nu)
        Act = empower.vbsp.project_modules.fun_ChooseProb.fun_ChooseProb([1-nu, nu],np.array([11, 12]))
        if Act == 11: # % Choose configuration @ (t-2)
            f_t[-1] = f_t[-3]          
        else: #Choose configuration @ (t-1)
            f_t[-1] = f_t[-2]        
        iExp = 0
        #print ('ok4')
    return f_t, u_t, iExp          

Appendix F
from __future__ import division
import numpy as np
import math
def fun_Sigmoid(beta, U_f): # U_f is only a value not a an array ??? 
    # U_f = np.random.random(5)
    #print(U_f )
    # U_f = np.sort(U_f)
    #print(U_f)
    # beta = 0.05
    
    U_f = np.array([U_f])
    #print ('U_f=', U_f)
    nChoice = len(U_f)
     
    tmp = np.dot(np.array([np.ones(nChoice)]),U_f)
    tmp = np.array(tmp)
    #print(tmp)
    theta = tmp - tmp.T
    #print(theta)
    p_f = np.array([np.zeros(nChoice)])
    #print(p_f)
    
    for k1 in range(nChoice):
        tmp2 = 0
        for k2 in range(nChoice):
            if (k1!= k2):
                tmp2 = tmp2 + math.exp(-beta*theta[k2][k1])
        p_f[0][k1] = 1/(1+tmp2)
    
    return p_f[0]











Appendix G
from __future__ import division
import numpy as np 
def fun_ChooseProb(P,X):
    '''#===============================================================================
    # % -------------------------------------------------------------------------
    # % fun_Chooserob randomly chooses an action x (configuration or choice) 
    # % depending on its probability p(x).
    # %
    # % Inputs:   P       - probability vector [p(x)]
    # %           x       - action vector [x]
    # % Outputs:  F       - chosen action
    # %
    # % Thant Zin Oo
    # % February 18, 2017.
    # % ------------------------------------------------------------------------- 
    #==============================================================================='''    
    cdf  = np.cumsum(P) # find cdf by taking cumulative sum.
    temp = np.random.uniform(0, 1) < cdf # check condition that rand is less than cdf    
    index = np.where(temp==1) # find the index of first true condition
    # print len(index),index     
    #print 'np.shape(X)=',np.shape(X)
    if len(index)!=0: 
        temp1 = np.array(index)            
        i =  temp1[[0],[0]]                         
        F = X[i] # choose the action with index.        
    else:
        print ('nothing happen! Check fun_ChooseProb function')
    return F






Appendix H
#!/bin/bash
while :
do
	clear
        # display menu
        echo "Server Name - $(hostname)"
	echo "-------------------------------"
	echo "     M A I N - M E N U"
	echo "-------------------------------"
	echo "Enter your password."
	echo "Press 1 to exit"	
        # get input from the user 
	read -p "Enter password:  " choice
        # make decision using case..in..esac 
	case $choice in
		hetnet1234)			
			echo "You are permitted to turn on this mobile phone!"				
			echo "Today is $(date)"
			read -p "Press [Enter] key to continue..." readEnterKey
			ORIGIN_PATH=$PWD
			THIS_SCRIPT_PATH=$(dirname $(readlink -f $0))
			source $THIS_SCRIPT_PATH/tools/build_helper
			i=0
			while true
			do
			    echo "$i"
			    i=$((i+=1))
			    echo "Executing UE agent...!"
			    cd /home/ue/openairinterface5g/
			    source oaienv 
			    cd /home/ue/openairinterface5g/cmake_targets/lte_build_oai/build			    
			    sudo -E ./lte-softmodem -U -C1910000000 -r25 --ue-scan-carrier --ue-txgain 70 --ue-rxgain 80 2>&1 -d | tee UE_TRA.log

			    trap handle_ctrl_c INT
			done

			;;
		1)
			echo "Bye!"
			exit 0
			;;
		*)
			echo "Wrong password"	
			read -p "Press [Enter] key to continue..." readEnterKey
			;;
	esac		
				
done

















Appendix E: Code for sending UE information to eNB:

a. Code in the UE agent

#include<stdio.h> //printf
#include<string.h> //memset
#include<stdlib.h> //exit(0);
#include<arpa/inet.h>
#include<sys/socket.h>

#define SERVER "192.168.100.101"
#define BUFLEN 4096  //Max length of buffer
#define PORT 3333   //The port on which to send data

void die(char *s)
{
    perror(s);
    exit(1);
}

int main(void)
{
    struct sockaddr_in si_other;
    int s, i, slen=sizeof(si_other),a;
    float b,c; 
    char buf[BUFLEN];
    char message[BUFLEN],old_message[BUFLEN]="\0",str[50];
    FILE *fp;
    if ( (s=socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP)) == -1)
    {
        die("socket");
    }

    memset((char *) &si_other, 0, sizeof(si_other));
    si_other.sin_family = AF_INET;
    si_other.sin_port = htons(PORT);

    if (inet_aton(SERVER , &si_other.sin_addr) == 0)
    {
        fprintf(stderr, "inet_aton() failed\n");
        exit(1);
    }
    while(1)
    {   
	fp=fopen("data.txt","r");
	if(fp !=NULL)
	{
	while(!feof(fp))	
	{
	fgets(str,20,fp);
	if(str[0]==56||(str[0]==49 && str[1]==48))	
	strcat(message,str);		
	}
	//puts(message);
	}
    	else
	printf("Could not find file");
 	fclose(fp);
         
        //send the message
	if(strcmp(old_message,message)!=0)
	{
        	if (sendto(s, message, strlen(message) , 0 , (struct sockaddr *) &si_other, slen)==-1)
        	{
            	die("sendto()");
        	}
	 strcpy(old_message,message);
	 memset(message,'\0', BUFLEN);
	}
        memset(buf,'\0', BUFLEN);
        //try to receive some data, this is a blocking call
        if (recvfrom(s, buf, BUFLEN, 0, (struct sockaddr *) &si_other, &slen) == -1)
        {
            die("recvfrom()");
        }
	 puts(buf);
    }  
    close(s);
    return 0;
}

b. Code in the eNB agent side
#include<stdio.h> //printf
#include<string.h> //memset
#include<stdlib.h> //exit(0);
#include<arpa/inet.h>
#include<sys/socket.h>
 
#define BUFLEN 512  //Max length of buffer
#define PORT 3333   //The port on which to listen for incoming data
 
void die(char *s)
{
    perror(s);
    exit(1);
}
 
int main(void)
{
    struct sockaddr_in si_me, si_other;
     
    int s, i, slen = sizeof(si_other) , recv_len;
    char buf[BUFLEN];
    FILE *fp; 
    //create a UDP socket
    if ((s=socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP)) == -1)
    {
        die("socket");
    }
     
    // zero out the structure
    memset((char *) &si_me, 0, sizeof(si_me));
     
    si_me.sin_family = AF_INET;
    si_me.sin_port = htons(PORT);
    si_me.sin_addr.s_addr = htonl(INADDR_ANY);
     
    //bind socket to port
    if( bind(s , (struct sockaddr*)&si_me, sizeof(si_me) ) == -1)
    {
        die("bind");
    }
     
    //keep listening for data
    while(1)
    {
        printf("Waiting for data...");
        fflush(stdout);
         
        //try to receive some data, this is a blocking call
        if ((recv_len = recvfrom(s, buf, BUFLEN, 0, (struct sockaddr *) &si_other, &slen)) == -1)
        {
            die("recvfrom()");
        }
         
        printf("Data: %s\n" , buf);
        fp=fopen("data.txt","w");
	if(fp !=NULL)
	{
	fputs(buf,fp);
	}
    	else
	printf("Could not find file");
 	fclose(fp); 
        //now reply the client with the same data
        if (sendto(s, buf, recv_len, 0, (struct sockaddr*) &si_other, slen) == -1)
        {
            die("sendto()");
        }
    }
 
    close(s);
    return 0;
}

 
Appendix I: Function sending information to eNB (Made by Mr. Alselme and Mr. Le Anh Tuan):

class VBSPConnection(object):
    """VBSP Connection.
    Represents a connection to a ENB (EUTRAN Base Station) using
    the VBSP Protocol. One VBSPConnection object is created for every
    ENB in the network. The object implements the logic for handling
    incoming messages. The currently supported messages are:

    Attributes:
        stream: The stream object used to talk with the ENB.
        address: The connection source address, i.e. the ENB IP address.
        server: Pointer to the server object.
        vbs: Pointer to a VBS object.
    """

    def __init__(self, stream, addr, server):
        self.stream = stream
        self.stream.set_nodelay(True)
        self.addr = addr
        self.server = server
        self.vbs = None
        self.seq = 0
        self.stream.set_close_callback(self._on_disconnect)
        self.__buffer = b''
        self._hb_interval_ms = 500
        self._hb_worker = tornado.ioloop.PeriodicCallback(self._heartbeat_cb,
                                                          self._hb_interval_ms)
        self.endian = sys.byteorder
        self._hb_worker.start()
        self._wait()

    def to_dict(self):
        """Return dict representation of object."""

        return self.addr

    def _heartbeat_cb(self):
        """Check if connection is still active."""

        if self.vbs and not self.stream.closed():
            timeout = (self.vbs.period / 1000) * 3
            if (self.vbs.last_seen_ts + timeout) < time.time():
                LOG.info('Client inactive %s at %r', self.vbs.addr, self.addr)
                #self.stream.close()

    def stream_send(self, message):



        """Send message."""
        transfer_data = 1
        transfer_data1 = 9.6
        transfer_data2 = 7.1
        transfer_data3 = 1.1

        # Update the sequence number of the messages
        message.head.seq = self.seq + 1
        #added for testing
        message.head.transfer_data = transfer_data
        message.head.transfer_data1 = transfer_data1
        message.head.transfer_data2 = transfer_data2
        message.head.transfer_data3 = transfer_data3

        MNO = Controller_Name('----Project Name: Markov approximation-based learning in 5G network---')
        # ==============================================================================
        M1 = [89.75, 89.75, 89.75]  # via BS id set at configuration file
        M2 = [21, 21, 21, 21, 21]  # via UE emei

        M3 = np.array([[0, 0, 1],
                       [0, 0, 1],
                       [1, 1, 0]])

        M4 = np.array([[1, 0, 0],
                       [0, 1, 0],
                       [0, 0, 1]])

        M5 = np.array([[-69.12372078, -74.1376763, -71.82325875],
                       [-53.83030764, -70.29361338, -74.97618152],
                       [-59.74909419, -67.796359, -75.62515563],
                       [-66.54979872, -74.95372667, -69.25830752],
                       [-61.29133112, -73.60238591, -70.5957919]])
        # ===============================================================================
        # print 'Getting SINR level'
        # MNO.P_Rx = 10**(0.1*MNO.P_Rx)
        # #print 'MNO.P_Rx', MNO.P_Rx
        # for k1 in range(MNO.nUE):
        #     for k2 in range(MNO.nBS):
        #         MNO.Intf_UExBS_RB[[k1],[k2]] = np.dot(MNO.P_Rx[[k1],:], MNO.BS_Rmap[:,[k2]]) # Wats
        #         MNO.SINR_UE_BS_RB[[k1],[k2]] = MNO.P_Rx[[k1],[k2]] / (MNO.Intf_UExBS_RB[[k1],[k2]]  + MNO.N0) # Wats
        #
        # SINR_dB = 10*np.log10(MNO.SINR_UE_BS_RB)
        M6 = MNO.Intf_UExBS_RB = np.array([[6.57164546e-08, 6.57164546e-08, 1.60925213e-07],
                                           [3.17966852e-08, 3.17966852e-08, 4.23316627e-06],
                                           [2.73832150e-08, 2.73832150e-08, 1.22557256e-06],
                                           [1.18623094e-07, 1.18623094e-07, 2.53281241e-07],
                                           [8.71807921e-08, 8.71807921e-08, 7.86419045e-07]])
        M7 = SINR_dB = np.array([[2.69953797, -2.31441755, -3.88949969],
                                 [21.14587388, 4.68256814, -21.24283479],
                                 [15.87606144, 7.82879663, -16.50854592],
                                 [2.7085088, -5.69541915, -3.29433778],
                                 [9.30446078, -3.00659401, -9.55233212]])

        R_U, LA_UA,LA_DPA,LA_DRBA= scheduling_algoirthm(M1, M2, M3, M4, M5, M6, M7)




        print ('result', R_U)

        LOG.info("Testing: version %s Data1 %s, Data2 %s , Data3 %s Head %s  Seq number %u", message.head.transfer_data , message.head.transfer_data1, message.head.transfer_data2, message.head.transfer_data3, message,
                 message.head.seq)
        #LOG.info("Connection from data %s data1 %s, data2 %s , data3 %s seq number %u", message.transfer_data, message.transfer_data1,
        #         message.transfer_data2, message.transfer_data3,
        #       message.head.seq)
        nBS =3
        for bs_id in range(nBS):
            # Send to eNB-1
            message.head.mUA=LA_UA[bs_id]
            message.head.mPA=LA_DPA[bs_id]
            message.head.GRB1 = LA_DRBA[0]
            message.head.GRB2 = LA_DRBA[1]
            message.head.GRB3 = LA_DRBA[2]
            message.head.GRB4 = LA_DRBA[3]
            message.head.GRB5 = LA_DRBA[4]

            size = message.ByteSize()
            #print(message.__str__())
            size_bytes = (socket.htonl(size)).to_bytes(4, byteorder=self.endian)
            send_buff = serialize_message(message)
            buff = size_bytes + send_buff

            if buff is None:
                LOG.error("errno %u occured")
            self.stream.write(buff)
            if bs_id ==0:
                # #added by anselme
                address = ('192.168.100.101', 2210)
                sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
                sock.connect(address)
                sock.sendall(buff)
                #self.stream.write(buff)
                print ('message.head.mPA=',message.head.mPA)
                print ('sending to bs ', bs_id)
            if bs_id ==1:
                # #added by anselme
                address = ('192.168.100.102', 2210)
                sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
                sock.connect(address)
                sock.sendall(buff)
                #self.stream.write(buff)
                print ('message.head.mPA=', message.head.mPA)
                print ('sending to bs ', bs_id)
            if bs_id ==2:
                # #added by anselme
                address = ('192.168.100.103', 2210)
                sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
                sock.connect(address)
                sock.sendall(buff)
                #self.stream.write(buff)
                print ('message.head.mPA=', message.head.mPA)
                print ('sending to bs ', bs_id)






See Appendix K: Decoding data at the eNB agent:

///////////////////////////////Made by Mr. LE ANH TUAN, Tested by Mr. Alseme/////////////////////////////////////////////////////////////
//
//				// getting information sent from controller:
				net_process_message(net, msg);
				double HeaderVersion = msg->head->vers;
				int BaseStation_ID = msg->head->b_id;
				double ControllerSequenceNumber = msg->head->seq;
				double vector_PA = msg->head->mpa;
				double vector_UA = msg->head->mua;
				double vector_GRB1 = msg->head->grb1;
				double vector_GRB2 = msg->head->grb2;
				double vector_GRB3 = msg->head->grb3;
				double vector_GRB4 = msg->head->grb4;
				double vector_GRB5 = msg->head->grb5;
//				// converting to string variables: mpa, mua, grb1, grb2, grb3, grb4, grb5,
			    int n_mUA = 7; // length of vector UA
			    int n_mPA = 7; // length of vector PA
			    int n_mGRB = 9; // length of vector GRB
			    int n_UE = 5; // length of vector
			    int n_BS = 3; // length of vector
			    int n_RB = 25; // length of vector
			    int n_GRB = 6; // number of RBs per each group
//
			    char s_vector_PA[n_mPA];
			    char s_vector_UA[n_mUA];
			    char s_vector_GRB1[n_mGRB];
			    char s_vector_GRB2[n_mGRB];
			    char s_vector_GRB3[n_mGRB];
			    char s_vector_GRB4[n_mGRB];
			    char s_vector_GRB5[n_mGRB];
//
//			    // converting process to string:
			    snprintf(s_vector_PA, n_mPA, "%f", vector_PA);
			    snprintf(s_vector_UA, n_mUA, "%f", vector_UA);
			    snprintf(s_vector_GRB1, n_mGRB, "%f", vector_GRB1);
			    snprintf(s_vector_GRB2, n_mGRB, "%f", vector_GRB2);
			    snprintf(s_vector_GRB3, n_mGRB, "%f", vector_GRB3);
			    snprintf(s_vector_GRB4, n_mGRB, "%f", vector_GRB4);
			    snprintf(s_vector_GRB5, n_mGRB, "%f", vector_GRB5);
//
//			    // get private information from SDN_controller side:
//			    // creating pointers:
			    char *ps_vector_PA=s_vector_PA;
			    char *ps_vector_UA=s_vector_UA;
			    char *ps_vector_GRB1=s_vector_GRB1;
			    char *ps_vector_GRB2=s_vector_GRB2;
			    char *ps_vector_GRB3=s_vector_GRB3;
			    char *ps_vector_GRB4=s_vector_GRB4;
			    char *ps_vector_GRB5=s_vector_GRB5;
//			    // init
			    int i,j;
			    int p_Tx; // value of power is defined with maximum 99 dB
                int m_UA[n_UE]; // matrix of UA allocation
                for (i=0;i<n_UE;i++)
                {
                	m_UA[i] =0;
                }
                int m_RBA[n_UE][n_RB]; // matrix of RB allocation
                for (i=0;i<n_UE;i++)
                {
                    for (j=0;j<n_RB;j++)
                    {

                    	m_RBA[i][j] =0;
                    }
                }
                char ps_Tx[2];
                char ps_BS[1];

//			    // Updating GRB information from all GRBs
			    // GRB1: from RB0 to RB4
			    for(i = 1; i <= (n_GRB-1); i++) { // GRB1
//			    	/// ps_vector_GRB1 = 100200
			    	char s_ue_id[1];
			    	slice_str(ps_vector_GRB1,s_ue_id,i,i);
			    	//s_ue_id = ps_vector_GRB1[i];
//			    	// converting string to int
			    	int ue_id = atoi(s_ue_id);
			    	if (ue_id != 0)
			    	{
			    		m_RBA[ue_id-1][0+i-1] = 1; // updating to mRBA matrix
			    	}
			    }






			    //			    // GRB2: from RB5 to RB9
			    for(i = 1; i <= (n_GRB-1); i++) { // GRB1
//			    	/// ps_vector_GRB1 = 100200
			    	char s_ue_id[1];
			    	slice_str(ps_vector_GRB2,s_ue_id,i,i);
			    	//s_ue_id = ps_vector_GRB1[i];
//			    	// converting string to int
			    	int ue_id = atoi(s_ue_id);
			    	if (ue_id != 0)
			    	{
			    		m_RBA[ue_id-1][5+i-1] = 1; // updating to mRBA matrix
			    	}

 			    }
//			    // GRB3: from RB10 to RB14
			    for(i = 1; i <= (n_GRB-1); i++) { // GRB1
//			    	/// ps_vector_GRB1 = 100200
			    	char s_ue_id[1];
			    	slice_str(ps_vector_GRB3,s_ue_id,i,i);
			    	//s_ue_id = ps_vector_GRB1[i];
//			    	// converting string to int
			    	int ue_id = atoi(s_ue_id);
			    	if (ue_id != 0)
			    	{
			    		m_RBA[ue_id-1][10+i-1] = 1; // updating to mRBA matrix
			    	}

			    }
//			    // GRB4: from RB15 to RB19
			    for(i = 1; i <= (n_GRB-1); i++) { // GRB1
			    	/// ps_vector_GRB1 = 100200
			    	char s_ue_id[1];
			    	slice_str(ps_vector_GRB4,s_ue_id,i,i);
			    	//s_ue_id = ps_vector_GRB1[i];
//			    	// converting string to int
			    	int ue_id = atoi(s_ue_id);
			    	if (ue_id != 0)
			    	{
			    		m_RBA[ue_id-1][15+i-1] = 1; // updating to mRBA matrix
			    	}

			    }
//			    // GRB5: from RB21 to RB25
			    for(i = 1; i <= (n_GRB-1); i++) { // GRB1
//			    	/// ps_vector_GRB1 = 100200
			    	char s_ue_id[1];
			    	slice_str(ps_vector_GRB5,s_ue_id,i,i);
			    	//s_ue_id = ps_vector_GRB1[i];
//			    	// converting string to int
			    	int ue_id = atoi(s_ue_id);
			    	if (ue_id != 0)
			    	{
			    		m_RBA[ue_id-1][20+i-1] = 1; // updating to mRBA matrix
			    	}

			    }
//
//			    // Updating power and UA information to array
//
			    switch(BaseStation_ID)
			    {
			    case 3618:
				    slice_str(ps_vector_PA, ps_Tx, 0, 1); // updating transmit power to BS-3618
				    p_Tx = atoi(ps_Tx);
//				    printf("%s\n", p_Tx);
				    // updating UA to BS-3618
				    for (i=1; i<=n_UE; i++) // we start from 1 in the vector
				    {
				    	char s_bs_id[1];
				    	slice_str(ps_vector_UA,s_bs_id,i,i);
				    	int bs_id = atoi(s_bs_id);
				    	if (bs_id==1) // this is compared to string ???
				    	{
				    		m_UA[i-1] = 1; // update to UA matrix (mUA). (i-1) is located from possion 0
				    	}
				    }
			    	break;
			    case 3619:
				    slice_str(ps_vector_PA, ps_Tx, 2, 3); // updating transmit power to BS-3619
				    p_Tx = atoi(ps_Tx);
//				    printf("%s\n", p_Tx);

				    for (i=1; i<=n_UE; i++) // we start from 1 in the vector
				    {
				    	char s_bs_id[1];
				    	slice_str(ps_vector_UA,s_bs_id,i,i);
				    	int bs_id = atoi(s_bs_id);
				    	if (bs_id==2) // this is compared to string ???
				    	{
				    		m_UA[i-1] = 1; // update to UA matrix (mUA). (i-1) is located from possion 0
				    	}
				    }
////                    // print m_UA result:
//				    for(int i = 0; i <= (n_UE-1); i++) {
//				            printf("%i ", m_UA[i]);
//				    }
			    	break;
			    case 3620:
				    slice_str(ps_vector_PA, ps_Tx, 4, 5); // updating transmit power to BS-3620
				    p_Tx = atoi(ps_Tx);

//				    printf("%s\n", p_Tx);
				    for (i=1; i<=n_UE; i++) // we start from 1 in the vector
				    {
				    	char s_bs_id[1];
				    	slice_str(ps_vector_UA,s_bs_id,i,i);
				    	int bs_id = atoi(s_bs_id);
				    	if (bs_id==3) // this is compared to string ???
				    	{
				    		m_UA[i-1] = 1; // update to UA matrix (mUA). (i-1) is located from possion 0
				    	}

				    }
//                    // print m_UA result:
//				    for(int i = 0; i <= (n_UE-1); i++) {
//				            printf("%i ", m_UA[i]);
//				    }
			    	break;
			    }
//
			    printf("Converting is completed!");
//
                printf("print m_UA result:");
			    for(i = 0; i <= (n_UE-1); i++) {
			            printf("%i ", m_UA[i]);
			    }
			    printf("print p_Tx result:");
			    printf("%i \n", p_Tx);
//
                printf("print m_RBA result:");
                int row, columns;
                for (row=0; row<(n_UE-1); row++)
                {
                    for(columns=0; columns<(n_RB-1); columns++)
                         printf("%d     ", m_RBA[row][columns]);
                    printf("\n");
                 }
//////////////////////End of updating data base///////////////////////////////////////////////////////////////////////
















Appendix L: Coding data at the eNB agent before sending to SDN controller.

//// Made by MR. LE ANH TUAN --> tested.  ///
void vector_to_str(double *input, char *output)
// input: vector
// output: string
// n: lenth for each entity. For example: -195.7 --> 1957 --> n = 4
// example: v= [-95.6 -53.4 -83.7]
{   int n = 5;



    int i=0;
    int i1;
    double num;
    for (i1 = 0; i1<3; i1++)
    {
    	num = input[i1];
    	//printf("num: %f", num);


    	char str[n+1];
    	snprintf(str,n+1,"%f",num); // convert to string
    	int i2;
        for (i2=1;i2<=n-1;i2++) // ignoring the "-" sign
        {
        	i= i+1;
        	output[i] = str[i2]; // getting characters
        	//printf ("%s", str[i2]);
        }
    }
}

void vector_to_str_ss(double *input, char *output)
{   int n = 2;



    int i=0;
    int i1;
    double num;
    for (i1 = 0; i1<5; i1++)
    {
    	num = input[i1];
    	//printf("num: %f", num);

    	char str[n+1];
    	snprintf(str,n+1,"%f",num); // convert to string
    	int i2;
        for (i2=0;i2<=n-2;i2++) // ignoring the "-" sign
        {
        	i= i+1;
        	output[i] = str[i2]; // getting characters
        	//printf ("%s", str[i2]);
        }
    }
}
double *vP_Rx1; // size of spectrum sensing results (SSR) of each RB
double *vP_Rx2;
double *vP_Rx3;
double *vP_Rx4;
double *vP_Rx5;

double *vRSRP1; // size of SINR from each UE and each BS (downlink)
double *vRSRP2; // size of SINR from each UE and each BS (downlink)
double *vRSRP3; // size of SINR from each UE and each BS (downlink)
double *vRSRP4; // size of SINR from each UE and each BS (downlink)
double *vRSRP5; // size of SINR from each UE and each BS (downlink)

double *vSSR1; // for GRB1
double *vSSR2; // for GRB2
double *vSSR3; // for GRB3
double *vSSR4; // for GRB4
double *vSSR5; // for GRB5


//double vP_Rx11[3] = {-7110, -7501, -7801};       // UE getting from UE1 for BS1, BS2, BS3; ---> will be updated from Mrs. Tra and Mr. Anupam
double vP_Rx11[3] = {-7110, -7501, -7801};       // UE getting from UE1 for BS1, BS2, BS3; ---> will be updated from Mrs. Tra and Mr. Anupam
vP_Rx1 = vP_Rx11;
double vP_Rx21[3] = {-7620, -4502, -7202};       // UE getting from UE2 for BS1, BS2, BS3; ---> will be updated from Mrs. Tra and Mr. Anupam
vP_Rx2 = vP_Rx21;
double vP_Rx31[3] = {-1413, -1753, -1903};   // // UE getting from UE3 for BS1, BS2, BS3; do not update
vP_Rx3 = vP_Rx31;
double vP_Rx41[3] = {-1714, -1754, -1784};   // // UE getting from UE4 for BS1, BS2, BS3; do not update
vP_Rx4 = vP_Rx41;
double vP_Rx51[3] = {-1715, -1755, -1785};  // // UE getting from UE5 for BS1, BS2, BS3; dBm, do not update,
vP_Rx5 = vP_Rx51;

double vRSRP11[3] = {-7100, -7500, -7800};  // RSVP from UE 1   ---> will be updated from Mrs. Tra and Mr. Anupam
vRSRP1 = vRSRP11;
double vRSRP21[3] = {-7600, -4500, -7200};  // RSVP from UE 2   ---> will be updated from Mrs. Tra and Mr. Anupam
vRSRP2 = vRSRP21;
double vRSRP31[3] = {-4100, -7500, -9000}; // RSVP from UE 3  do not update
vRSRP3 = vRSRP31;
double vRSRP41[3] = {-7100, -7500, -7800}; // RSVP from UE 4  do not update
vRSRP4 = vRSRP41;
double vRSRP51[3] = {-7100, -7500, -7800}; // RSVP from UE 5  do not update
vRSRP5 = vRSRP51;
	//
double vSSR11[5] = {1,0,0,0,1};// 1 : RB is not available, 0: available RB
vSSR1 = vSSR11;
double vSSR21[5] = {0,0,0,0,1};// 1 : RB is not available, 0: available RB
vSSR2 = vSSR21;
double vSSR31[5] = {0,0,1,0,0};// 1 : RB is not available, 0: available RB
vSSR3 = vSSR31;
double vSSR41[5] = {0,1,1,0,0};// 1 : RB is not available, 0: available RB
vSSR4 = vSSR41;
double vSSR51[5] = {0,0,1,0,0};// 1 : RB is not available, 0: available RB
vSSR5 = vSSR51;


//    printf("print m_UA result:");
//    for(int i = 0; i <= 2; i++) {
//            printf("%f ", vP_Rx11[i]);
//    }
//    printf("\n");
//    vP_Rx1 = vP_Rx11;
//    printf("print vP_Rx1 result:");
//    for(int i = 0; i <= 2; i++) {
//            printf("%f ", vP_Rx1[i]);
//    }
//    printf("\n");
char sP_Rx1[13] = "10000000000000";
char sP_Rx2[13] = "10000000000000";
char sP_Rx3[13] = "10000000000000";
char sP_Rx4[13] = "10000000000000";
char sP_Rx5[13] = "10000000000000";

char sRSRP1[13] = "10000000000000";
char sRSRP2[13] = "10000000000000";
char sRSRP3[13] = "10000000000000";
char sRSRP4[13] = "10000000000000";
char sRSRP5[13] = "10000000000000";

char sSSR1[13] = "100000";
char sSSR2[13] = "100000";
char sSSR3[13] = "100000";
char sSSR4[13] = "100000";
char sSSR5[13] = "100000";

vector_to_str(vP_Rx1, sP_Rx1);
vector_to_str(vP_Rx2, sP_Rx2);
vector_to_str(vP_Rx3, sP_Rx3);
vector_to_str(vP_Rx4, sP_Rx4);
vector_to_str(vP_Rx5, sP_Rx5);


vector_to_str(vRSRP1, sRSRP1);
vector_to_str(vRSRP2, sRSRP2);
vector_to_str(vRSRP3, sRSRP3);
vector_to_str(vRSRP4, sRSRP4);
vector_to_str(vRSRP5, sRSRP5);
	//
vector_to_str_ss(vSSR1, sSSR1);
vector_to_str_ss(vSSR2, sSSR2);
vector_to_str_ss(vSSR3, sSSR3);
vector_to_str_ss(vSSR4, sSSR4);
vector_to_str_ss(vSSR5, sSSR5);

printf("print sP_Rx1 result: %s \n",sP_Rx1);
printf("print sP_Rx2 result: %s \n",sP_Rx2);
printf("print sP_Rx3 result: %s \n",sP_Rx3);
printf("print sP_Rx4 result: %s \n",sP_Rx4);
printf("print sP_Rx5 result: %s \n",sP_Rx5);

printf("print sRSRP1 result: %s \n",sRSRP1);
printf("print sRSRP2 result: %s \n",sRSRP2);
printf("print sRSRP3 result: %s \n",sRSRP3);
printf("print sRSRP4 result: %s \n",sRSRP4);
printf("print sRSRP5 result: %s \n",sRSRP5);

printf("print sSSR1 result: %s \n",sSSR1);
printf("print sSSR2 result: %s \n",sSSR2);
printf("print sSSR3 result: %s \n",sSSR3);
printf("print sSSR4 result: %s \n",sSSR4);
printf("print sSSR5 result: %s \n",sSSR5);


double p_ue_rx1 = atof(sP_Rx1); // 1086004400210; // dowlink transmit power or Tx_gain
double p_ue_rx2 = atof(sP_Rx2);// 1086004400220; // dowlink transmit power or Tx_gain
double p_ue_rx3 = atof(sP_Rx3);// 1175017501750; // dowlink transmit power or Tx_gain 175: NO ue
double p_ue_rx4 = atof(sP_Rx4);// 1175017501750; // dowlink transmit power or Tx_gain
double p_ue_rx5 = atof(sP_Rx5);// 1175017501750; // dowlink transmit power or Tx_gain
//
double rsrp1 = atof(sRSRP1); //vRSRP1// 1075007600770; // dowlink transmit power or Tx_gain 075: -75 dBm
double rsrp2 = atof(sRSRP2); //=  1079007200750; // dowlink transmit power or Tx_gain
double rsrp3 = atof(sRSRP3); //= 1175017501750; // dowlink transmit power or Tx_gain // NO ue
double rsrp4 = atof(sRSRP4); //1175017501750; // dowlink transmit power or Tx_gain // NO ue
double rsrp5 = atof(sRSRP5); //= 1175017501750; // dowlink transmit power or Tx_gain // nO ue
//
double spectrum_sensing_grb1 = atof(sSSR1);//101011; // will get from sensing function
double spectrum_sensing_grb2 = atof(sSSR2);//201011; // will get from sensing function
double spectrum_sensing_grb3 = atof(sSSR3);//311011; // will get from sensing function
double spectrum_sensing_grb4 = atof(sSSR4);//401101; // will get from sensing function
double spectrum_sensing_grb5 = atof(sSSR5);//511011; // will get from sensing function
//// end of code///

// assigning to buffer for transmitting data to controller.



// made by Mr. Aselme --> tested
//double p_ue_rx1 = 1086004400210; // dowlink transmit power or Tx_gain
//double p_ue_rx2 = = 1086004400220; // dowlink transmit power or Tx_gain
//double p_ue_rx3 = 1175017501751; // dowlink transmit power or Tx_gain 175: NO ue
//double p_ue_rx4 = 1175017501750; // dowlink transmit power or Tx_gain
//double p_ue_rx5 = 1175017501750; // dowlink transmit power or Tx_gain
//
//double rsrp1 = 1075007600770; // dowlink transmit power or Tx_gain 075: -75 dBm
//double rsrp2 = 1079007200750; // dowlink transmit power or Tx_gain
//double rsrp3 = 1175017501750; // dowlink transmit power or Tx_gain // NO ue
//double rsrp4 = 1175017501750; // dowlink transmit power or Tx_gain // NO ue
//double rsrp5 = 1175017501750; // dowlink transmit power or Tx_gain // nO ue
//
//double spectrum_sensing_grb1 = 101011; // will get from sensing function
//double spectrum_sensing_grb2 = 201011; // will get from sensing function
//double spectrum_sensing_grb3 = 311011; // will get from sensing function
//double spectrum_sensing_grb4 = 401101; // will get from sensing function
//double spectrum_sensing_grb5 = 511011; // will get from sensing function

double td1=spectrum_sensing_grb1;
double td2=spectrum_sensing_grb2;
double td3=spectrum_sensing_grb3;
double td4=spectrum_sensing_grb4;
double td5=spectrum_sensing_grb5;
double td6=spectrum_sensing_grb5;

double td7=p_ue_rx1;
double td8=p_ue_rx2;
double td9=p_ue_rx3;
double td10=p_ue_rx4;
double td11=p_ue_rx5;

double td12=rsrp1;
double td13=rsrp2;
double td14=rsrp3;
double td15=rsrp4;
double td16=rsrp5;

double td17=0;
double td18=0;
double td19=0;
double td20=0;


//receiving from controller
double mua=1.0;
double mpa=2.5;
double grb1=58.0;
double grb2=58.0;
double grb3=58.0;
double grb4=45.5;
double grb5=12.0;

//end of code

//Testing unpacked message from net.c



Appendix P: User Association

int initial_sync(PHY_VARS_UE *phy_vars_ue, runmode_t mode)
{

  int32_t sync_pos,sync_pos2,sync_pos_slot;
  int32_t metric_fdd_ncp=0,metric_fdd_ecp=0,metric_tdd_ncp=0,metric_tdd_ecp=0;
  uint8_t phase_fdd_ncp,phase_fdd_ecp,phase_tdd_ncp,phase_tdd_ecp;
  uint8_t flip_fdd_ncp,flip_fdd_ecp,flip_tdd_ncp,flip_tdd_ecp;
  //  uint16_t Nid_cell_fdd_ncp=0,Nid_cell_fdd_ecp=0,Nid_cell_tdd_ncp=0,Nid_cell_tdd_ecp=0;
  LTE_DL_FRAME_PARMS *frame_parms = &phy_vars_ue->lte_frame_parms;
  LOG_I(PHY,"[TAIHM][UE%d] Initial sync : ue->Nid_cell: %d\n",phy_vars_ue->Mod_id,phy_vars_ue->lte_frame_parms.Nid_cell);
  LOG_I(PHY,"[TAIHM][UE%d] Initial sync : ue->eNB_id: %d\n",phy_vars_ue->Mod_id,phy_vars_ue->lte_ue_common_vars.eNb_id);
  LOG_I(PHY,"[TAIHM][UE%d] Initial sync : ue->Nid_cell: %d\n",phy_vars_ue->Mod_id,frame_parms->Nid_cell);
  int ret=-1;
  int aarx,rx_power=0;

  /*#ifdef OAI_USRP
  __m128i *rxdata128;
  #endif*/
  //  LOG_I(PHY,"**************************************************************\n");
  // First try FDD normal prefix
  frame_parms->Ncp=NORMAL;
  frame_parms->frame_type=FDD;
  init_frame_parms(frame_parms,1);

  /*
  write_output("rxdata0.m","rxd0",phy_vars_ue->lte_ue_common_vars.rxdata[0],10*frame_parms->samples_per_tti,1,1);
  exit(-1);
  */
  sync_pos = lte_sync_time(phy_vars_ue->lte_ue_common_vars.rxdata,
                           frame_parms,
                           (int *)&phy_vars_ue->lte_ue_common_vars.eNb_id);

  //  write_output("rxdata1.m","rxd1",phy_vars_ue->lte_ue_common_vars.rxdata[0],10*frame_parms->samples_per_tti,1,1);
  if (sync_pos >= frame_parms->nb_prefix_samples)
    sync_pos2 = sync_pos - frame_parms->nb_prefix_samples;
  else
    sync_pos2 = sync_pos + FRAME_LENGTH_COMPLEX_SAMPLES - frame_parms->nb_prefix_samples;

#ifdef DEBUG_INITIAL_SYNCH
  LOG_I(PHY,"[UE%d] Initial sync : Estimated PSS position %d, Nid2 %d\n",phy_vars_ue->Mod_id,sync_pos,phy_vars_ue->lte_ue_common_vars.eNb_id);
#endif

  // SSS detection

  // PSS is hypothesized in last symbol of first slot in Frame
  sync_pos_slot = (frame_parms->samples_per_tti>>1) - frame_parms->ofdm_symbol_size - frame_parms->nb_prefix_samples;

  if (sync_pos2 >= sync_pos_slot)
    phy_vars_ue->rx_offset = sync_pos2 - sync_pos_slot;
  else
    phy_vars_ue->rx_offset = FRAME_LENGTH_COMPLEX_SAMPLES + sync_pos2 - sync_pos_slot;

  if (((sync_pos2 - sync_pos_slot) >=0 ) &&
      ((sync_pos2 - sync_pos_slot) < ((FRAME_LENGTH_COMPLEX_SAMPLES-frame_parms->samples_per_tti/2)))) {
#ifdef DEBUG_INITIAL_SYNCH
    LOG_I(PHY,"Calling sss detection (FDD normal CP)\n");
#endif
    LOG_I(PHY,"[TAIHM][UE%d] Initial sync, Nid_cell before rx_sss: %d\n",phy_vars_ue->Mod_id,frame_parms->Nid_cell);
    rx_sss(phy_vars_ue,&metric_fdd_ncp,&flip_fdd_ncp,&phase_fdd_ncp);
    LOG_I(PHY,"[TAIHM][UE%d] Initial sync, Nid_cell after rx_sss: %d\n",phy_vars_ue->Mod_id,frame_parms->Nid_cell);
    frame_parms->nushift  = frame_parms->Nid_cell%6;

    if (flip_fdd_ncp==1)
      phy_vars_ue->rx_offset += (FRAME_LENGTH_COMPLEX_SAMPLES>>1);

    init_frame_parms(&phy_vars_ue->lte_frame_parms,1);
    lte_gold(frame_parms,phy_vars_ue->lte_gold_table[0],frame_parms->Nid_cell);
    ret = pbch_detection(phy_vars_ue,mode);
    //   write_output("rxdata2.m","rxd2",phy_vars_ue->lte_ue_common_vars.rxdata[0],10*frame_parms->samples_per_tti,1,1);

#ifdef DEBUG_INITIAL_SYNCH
    LOG_I(PHY,"FDD Normal prefix: CellId %d metric %d, phase %d, flip %d, pbch %d\n",
          frame_parms->Nid_cell,metric_fdd_ncp,phase_fdd_ncp,flip_fdd_ncp,ret);
#endif
  } else {
#ifdef DEBUG_INITIAL_SYNCH
    LOG_I(PHY,"FDD Normal prefix: SSS error condition: sync_pos %d, sync_pos_slot %d\n", sync_pos, sync_pos_slot);
#endif
  }


  if (ret==-1) {

    // Now FDD extended prefix
    frame_parms->Ncp=EXTENDED;
    frame_parms->frame_type=FDD;
    init_frame_parms(frame_parms,1);

    if (sync_pos < frame_parms->nb_prefix_samples)
      sync_pos2 = sync_pos + FRAME_LENGTH_COMPLEX_SAMPLES - frame_parms->nb_prefix_samples;
    else
      sync_pos2 = sync_pos - frame_parms->nb_prefix_samples;

    // PSS is hypothesized in last symbol of first slot in Frame
    sync_pos_slot = (frame_parms->samples_per_tti>>1) - frame_parms->ofdm_symbol_size - (frame_parms->nb_prefix_samples);

    if (sync_pos2 >= sync_pos_slot)
      phy_vars_ue->rx_offset = sync_pos2 - sync_pos_slot;
    else
      phy_vars_ue->rx_offset = FRAME_LENGTH_COMPLEX_SAMPLES + sync_pos2 - sync_pos_slot;

    //msg("nb_prefix_samples %d, rx_offset %d\n",frame_parms->nb_prefix_samples,phy_vars_ue->rx_offset);

    if (((sync_pos2 - sync_pos_slot) >=0 ) &&
        ((sync_pos2 - sync_pos_slot) < ((FRAME_LENGTH_COMPLEX_SAMPLES-frame_parms->samples_per_tti/2)))) {

      rx_sss(phy_vars_ue,&metric_fdd_ecp,&flip_fdd_ecp,&phase_fdd_ecp);
      frame_parms->nushift  = frame_parms->Nid_cell%6;

      if (flip_fdd_ecp==1)
        phy_vars_ue->rx_offset += (FRAME_LENGTH_COMPLEX_SAMPLES>>1);

      init_frame_parms(&phy_vars_ue->lte_frame_parms,1);
      lte_gold(frame_parms,phy_vars_ue->lte_gold_table[0],frame_parms->Nid_cell);
      ret = pbch_detection(phy_vars_ue,mode);
      //     write_output("rxdata3.m","rxd3",phy_vars_ue->lte_ue_common_vars.rxdata[0],10*frame_parms->samples_per_tti,1,1);
#ifdef DEBUG_INITIAL_SYNCH
      LOG_I(PHY,"FDD Extended prefix: CellId %d metric %d, phase %d, flip %d, pbch %d\n",
            frame_parms->Nid_cell,metric_fdd_ecp,phase_fdd_ecp,flip_fdd_ecp,ret);
#endif
    } else {
#ifdef DEBUG_INITIAL_SYNCH
      LOG_I(PHY,"FDD Extended prefix: SSS error condition: sync_pos %d, sync_pos_slot %d\n", sync_pos, sync_pos_slot);
#endif
    }

    if (ret==-1) {
      // Now TDD normal prefix
      frame_parms->Ncp=NORMAL;
      frame_parms->frame_type=TDD;
      init_frame_parms(frame_parms,1);

      if (sync_pos >= frame_parms->nb_prefix_samples)
        sync_pos2 = sync_pos - frame_parms->nb_prefix_samples;
      else
        sync_pos2 = sync_pos + FRAME_LENGTH_COMPLEX_SAMPLES - frame_parms->nb_prefix_samples;

      // PSS is hypothesized in 2nd symbol of third slot in Frame (S-subframe)
      sync_pos_slot = frame_parms->samples_per_tti +
                      (frame_parms->ofdm_symbol_size<<1) +
                      frame_parms->nb_prefix_samples0 +
                      (frame_parms->nb_prefix_samples);

      if (sync_pos2 >= sync_pos_slot)
        phy_vars_ue->rx_offset = sync_pos2 - sync_pos_slot;
      else
        phy_vars_ue->rx_offset = (FRAME_LENGTH_COMPLEX_SAMPLES>>1) + sync_pos2 - sync_pos_slot;

      /*if (((sync_pos2 - sync_pos_slot) >=0 ) &&
      ((sync_pos2 - sync_pos_slot) < ((FRAME_LENGTH_COMPLEX_SAMPLES-frame_parms->samples_per_tti/2)))) {*/


      rx_sss(phy_vars_ue,&metric_tdd_ncp,&flip_tdd_ncp,&phase_tdd_ncp);

      if (flip_tdd_ncp==1)
        phy_vars_ue->rx_offset += (FRAME_LENGTH_COMPLEX_SAMPLES>>1);

      frame_parms->nushift  = frame_parms->Nid_cell%6;
      init_frame_parms(&phy_vars_ue->lte_frame_parms,1);

      lte_gold(frame_parms,phy_vars_ue->lte_gold_table[0],frame_parms->Nid_cell);
      ret = pbch_detection(phy_vars_ue,mode);
      //      write_output("rxdata4.m","rxd4",phy_vars_ue->lte_ue_common_vars.rxdata[0],10*frame_parms->samples_per_tti,1,1);

#ifdef DEBUG_INITIAL_SYNCH
      LOG_I(PHY,"TDD Normal prefix: CellId %d metric %d, phase %d, flip %d, pbch %d\n",
            frame_parms->Nid_cell,metric_tdd_ncp,phase_tdd_ncp,flip_tdd_ncp,ret);
#endif
      /*}
          else {
      #ifdef DEBUG_INITIAL_SYNCH
              LOG_I(PHY,"TDD Normal prefix: SSS error condition: sync_pos %d, sync_pos_slot %d\n", sync_pos, sync_pos_slot);
      #endif
      }*/


      if (ret==-1) {
        // Now TDD extended prefix
        frame_parms->Ncp=EXTENDED;
        frame_parms->frame_type=TDD;
        init_frame_parms(frame_parms,1);
        sync_pos2 = sync_pos - frame_parms->nb_prefix_samples;

        if (sync_pos >= frame_parms->nb_prefix_samples)
          sync_pos2 = sync_pos - frame_parms->nb_prefix_samples;
        else
          sync_pos2 = sync_pos + FRAME_LENGTH_COMPLEX_SAMPLES - frame_parms->nb_prefix_samples;

        // PSS is hypothesized in 2nd symbol of third slot in Frame (S-subframe)
        sync_pos_slot = frame_parms->samples_per_tti + (frame_parms->ofdm_symbol_size<<1) + (frame_parms->nb_prefix_samples<<1);

        if (sync_pos2 >= sync_pos_slot)
          phy_vars_ue->rx_offset = sync_pos2 - sync_pos_slot;
        else
          phy_vars_ue->rx_offset = (FRAME_LENGTH_COMPLEX_SAMPLES>>1) + sync_pos2 - sync_pos_slot;

        /*if (((sync_pos2 - sync_pos_slot) >=0 ) &&
          ((sync_pos2 - sync_pos_slot) < ((FRAME_LENGTH_COMPLEX_SAMPLES-frame_parms->samples_per_tti/2)))) {*/

        rx_sss(phy_vars_ue,&metric_tdd_ecp,&flip_tdd_ecp,&phase_tdd_ecp);
        frame_parms->nushift  = frame_parms->Nid_cell%6;

        if (flip_tdd_ecp==1)
          phy_vars_ue->rx_offset += (FRAME_LENGTH_COMPLEX_SAMPLES>>1);

        init_frame_parms(&phy_vars_ue->lte_frame_parms,1);
        lte_gold(frame_parms,phy_vars_ue->lte_gold_table[0],frame_parms->Nid_cell);
        ret = pbch_detection(phy_vars_ue,mode);

	//	write_output("rxdata5.m","rxd5",phy_vars_ue->lte_ue_common_vars.rxdata[0],10*frame_parms->samples_per_tti,1,1);
#ifdef DEBUG_INITIAL_SYNCH
        LOG_I(PHY,"TDD Extended prefix: CellId %d metric %d, phase %d, flip %d, pbch %d\n",
              frame_parms->Nid_cell,metric_tdd_ecp,phase_tdd_ecp,flip_tdd_ecp,ret);
#endif
        /*}
        else {
        #ifdef DEBUG_INITIAL_SYNCH
          LOG_I(PHY,"TDD Extended prefix: SSS error condition: sync_pos %d, sync_pos_slot %d\n", sync_pos, sync_pos_slot);
        #endif
        }*/

      }
    }
  }

  if (ret==0) {  // PBCH found so indicate sync to higher layers and configure frame parameters

#ifdef DEBUG_INITIAL_SYNCH
    LOG_I(PHY,"[UE%d] In synch, rx_offset %d samples\n",phy_vars_ue->Mod_id, phy_vars_ue->rx_offset);
#endif

    if (phy_vars_ue->UE_scan_carrier == 0) {
      if (phy_vars_ue->mac_enabled==1) {
	LOG_I(PHY,"[UE%d] Sending synch status to higher layers\n",phy_vars_ue->Mod_id);
	//mac_resynch();
	mac_xface->dl_phy_sync_success(phy_vars_ue->Mod_id,phy_vars_ue->frame_rx,0,1);//phy_vars_ue->lte_ue_common_vars.eNb_id);
	phy_vars_ue->UE_mode[0] = PRACH;
      }
      else {
	phy_vars_ue->UE_mode[0] = PUSCH;
      }

      generate_pcfich_reg_mapping(frame_parms);
      generate_phich_reg_mapping(frame_parms);
      //    init_prach625(frame_parms);

      //phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors=0;
      phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors_conseq=0;
    //phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors_last=0;
    }

    LOG_I(PHY,"[UE %d] Frame %d RRC Measurements => rssi %3.1f dBm (dig %3.1f dB, gain %d), N0 %d dBm,  rsrp %3.1f dBm/RE, rsrq %3.1f dB\n",phy_vars_ue->Mod_id,
	  phy_vars_ue->frame_rx,
	  10*log10(phy_vars_ue->PHY_measurements.rssi)-phy_vars_ue->rx_total_gain_dB,
	  10*log10(phy_vars_ue->PHY_measurements.rssi),
	  phy_vars_ue->rx_total_gain_dB,
	  phy_vars_ue->PHY_measurements.n0_power_tot_dBm,
	  10*log10(phy_vars_ue->PHY_measurements.rsrp[0])-phy_vars_ue->rx_total_gain_dB,
	  (10*log10(phy_vars_ue->PHY_measurements.rsrq[0])));
    
    
    LOG_I(PHY,"[UE %d] Frame %d MIB Information => %s, %s, NidCell %d, N_RB_DL %d, PHICH DURATION %d, PHICH RESOURCE %s, TX_ANT %d\n",
	  phy_vars_ue->Mod_id,
	  phy_vars_ue->frame_rx,
	  duplex_string[phy_vars_ue->lte_frame_parms.frame_type],
	  prefix_string[phy_vars_ue->lte_frame_parms.Ncp],
	  phy_vars_ue->lte_frame_parms.Nid_cell,
	  phy_vars_ue->lte_frame_parms.N_RB_DL,
	  phy_vars_ue->lte_frame_parms.phich_config_common.phich_duration,
	  phich_string[phy_vars_ue->lte_frame_parms.phich_config_common.phich_resource],
	  phy_vars_ue->lte_frame_parms.nb_antennas_tx_eNB);
#if defined(OAI_USRP) || defined(EXMIMO) || defined(OAI_LMSSDR)
    LOG_I(PHY,"[UE %d] Frame %d Measured Carrier Frequency %.0f Hz (offset %d Hz)\n",
	  phy_vars_ue->Mod_id,
	  phy_vars_ue->frame_rx,
	  openair0_cfg[0].rx_freq[0]-phy_vars_ue->lte_ue_common_vars.freq_offset,
	  phy_vars_ue->lte_ue_common_vars.freq_offset);
#endif




  } else {
#ifdef DEBUG_INITIAL_SYNC
    LOG_I(PHY,"[UE%d] Initial sync : PBCH not ok\n",phy_vars_ue->Mod_id);
    LOG_I(PHY,"[UE%d] Initial sync : Estimated PSS position %d, Nid2 %d\n",phy_vars_ue->Mod_id,sync_pos,phy_vars_ue->lte_ue_common_vars.eNb_id);
    /*      LOG_I(PHY,"[UE%d] Initial sync: (metric fdd_ncp %d (%d), metric fdd_ecp %d (%d), metric_tdd_ncp %d (%d), metric_tdd_ecp %d (%d))\n",
          phy_vars_ue->Mod_id,
          metric_fdd_ncp,Nid_cell_fdd_ncp,
          metric_fdd_ecp,Nid_cell_fdd_ecp,
          metric_tdd_ncp,Nid_cell_tdd_ncp,
          metric_tdd_ecp,Nid_cell_tdd_ecp);*/
    LOG_I(PHY,"[UE%d] Initial sync : Estimated Nid_cell %d, Frame_type %d\n",phy_vars_ue->Mod_id,
          frame_parms->Nid_cell,frame_parms->frame_type);
#endif

    phy_vars_ue->UE_mode[0] = NOT_SYNCHED;
    phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors_last=phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors;
    phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors++;
    phy_vars_ue->lte_ue_pbch_vars[0]->pdu_errors_conseq++;

  }

  // gain control
  if (ret!=0) { //we are not synched, so we cannot use rssi measurement (which is based on channel estimates)
    rx_power = 0;

    // do a measurement on the best guess of the PSS
    for (aarx=0; aarx<frame_parms->nb_antennas_rx; aarx++)
      rx_power += signal_energy(&phy_vars_ue->lte_ue_common_vars.rxdata[aarx][sync_pos2],
				frame_parms->ofdm_symbol_size+frame_parms->nb_prefix_samples);
    
    /*
    // do a measurement on the full frame
    for (aarx=0; aarx<frame_parms->nb_antennas_rx; aarx++)
      rx_power += signal_energy(&phy_vars_ue->lte_ue_common_vars.rxdata[aarx][0],
				frame_parms->samples_per_tti*10);
    */

    // we might add a low-pass filter here later
    phy_vars_ue->PHY_measurements.rx_power_avg[0] = rx_power/frame_parms->nb_antennas_rx; 

    phy_vars_ue->PHY_measurements.rx_power_avg_dB[0] = dB_fixed(phy_vars_ue->PHY_measurements.rx_power_avg[0]);

#ifdef DEBUG_INITIAL_SYNCH
  LOG_I(PHY,"[UE%d] Initial sync : Estimated power: %d dB\n",phy_vars_ue->Mod_id,phy_vars_ue->PHY_measurements.rx_power_avg_dB[0] );
#endif

#ifdef EXMIMO
  if ((openair_daq_vars.rx_gain_mode == DAQ_AGC_ON) &&
      (mode != rx_calib_ue) && (mode != rx_calib_ue_med) && (mode != rx_calib_ue_byp) )
    //phy_adjust_gain(phy_vars_ue,0);
    gain_control_all(phy_vars_ue->PHY_measurements.rx_power_avg_dB[0],0);

#else
#ifndef OAI_USRP
#ifndef OAI_BLADERF 
#ifndef OAI_LMSSDR
  phy_adjust_gain(phy_vars_ue,phy_vars_ue->PHY_measurements.rx_power_avg_dB[0],0);
#endif
#endif
#endif
#endif
  }
  else {
#ifdef EXMIMO
  if ((openair_daq_vars.rx_gain_mode == DAQ_AGC_ON) &&
      (mode != rx_calib_ue) && (mode != rx_calib_ue_med) && (mode != rx_calib_ue_byp) )
    //phy_adjust_gain(phy_vars_ue,0);
    gain_control_all(dB_fixed(phy_vars_ue->PHY_measurements.rssi),0);

#else
#ifndef OAI_USRP
#ifndef OAI_BLADERF 
#ifndef OAI_LMSSDR
  phy_adjust_gain(phy_vars_ue,dB_fixed(phy_vars_ue->PHY_measurements.rssi),0);
#endif
#endif
#endif
#endif
  }

  //  exit_fun("debug exit");
  return ret;
}

/*!
 * \brief This is the UE synchronize thread.
 * It performs band scanning and synchonization.
 * \param arg is a pointer to a \ref PHY_VARS_UE structure.
 * \returns a pointer to an int. The storage is not on the heap and must not be freed.
 */
static void *UE_thread_synch(void *arg)
{
	LOG_I( HW, "[lte-ue] [TAIHM] this start the UE thread synch\n");
  static int UE_thread_synch_retval;
  int i, hw_slot_offset;
  PHY_VARS_UE *UE = (PHY_VARS_UE*) arg;
  int current_band = 0;
  int current_offset = 0;
  sync_mode_t sync_mode = pbch;
  int card;
  int ind;
  int found;
  int freq_offset=0;

  uint8_t eNB_id_SDN = 8; //TAIHM added to test SDN functions
  uint8_t SDN_flag = 0;// TAIHM added for SDN controller
  FILE *SDN_file;

  UE->is_synchronized = 0;
  printf("UE_thread_sync in with PHY_vars_UE %p\n",arg);
  printf("waiting for sync (UE_thread_synch) \n");

#ifndef DEADLINE_SCHEDULER
  int policy, s, j;
  struct sched_param sparam;
  char cpu_affinity[1024];
  cpu_set_t cpuset;

  /* Set affinity mask to include CPUs 1 to MAX_CPUS */
  /* CPU 0 is reserved for UHD threads */
  CPU_ZERO(&cpuset);

  #ifdef CPU_AFFINITY
  if (get_nprocs() >2)
  {
    for (j = 1; j < get_nprocs(); j++)
      CPU_SET(j, &cpuset);

    s = pthread_setaffinity_np(pthread_self(), sizeof(cpu_set_t), &cpuset);
    if (s != 0)
    {
      perror( "pthread_setaffinity_np");
      exit_fun("Error setting processor affinity");
    }
  }
  #endif

  /* Check the actual affinity mask assigned to the thread */

  s = pthread_getaffinity_np(pthread_self(), sizeof(cpu_set_t), &cpuset);
  if (s != 0)
  {
    perror( "pthread_getaffinity_np");
    exit_fun("Error getting processor affinity ");
  }
  memset(cpu_affinity, 0 , sizeof(cpu_affinity));
  for (j = 0; j < CPU_SETSIZE; j++)
  if (CPU_ISSET(j, &cpuset))
  {  
     char temp[1024];
     sprintf(temp, " CPU_%d ", j);    
     strcat(cpu_affinity, temp);
  }

  memset(&sparam, 0 , sizeof (sparam));
  sparam.sched_priority = sched_get_priority_max(SCHED_FIFO)-1;
  policy = SCHED_FIFO ; 
  
  s = pthread_setschedparam(pthread_self(), policy, &sparam);
  if (s != 0)
     {
     perror("pthread_setschedparam : ");
     exit_fun("Error setting thread priority");
     }
  s = pthread_getschedparam(pthread_self(), &policy, &sparam);
  if (s != 0)
   {
     perror("pthread_getschedparam : ");
     exit_fun("Error getting thread priority");

   }

  LOG_I( HW, "[SCHED][UE] Started UE synch thread on CPU %d TID %ld , sched_policy = %s, priority = %d, CPU Affinity = %s \n", (int)sched_getcpu(), gettid(),
                   (policy == SCHED_FIFO)  ? "SCHED_FIFO" :
                   (policy == SCHED_RR)    ? "SCHED_RR" :
                   (policy == SCHED_OTHER) ? "SCHED_OTHER" :
                   "???",
                   (int) sparam.sched_priority, cpu_affinity);

#endif


  pthread_mutex_lock(&sync_mutex);
  printf("Locked sync_mutex, waiting (UE_sync_thread)\n");

  while (sync_var<0)
    pthread_cond_wait(&sync_cond, &sync_mutex);

  pthread_mutex_unlock(&sync_mutex);
  printf("unlocked sync_mutex (UE_sync_thread)\n");

  printf("starting UE synch thread (IC %d)\n",UE->instance_cnt_synch);
  ind = 0;
  found = 0;


  if (UE->UE_scan == 0) {
    do  {
      current_band = eutra_bands[ind].band;
      printf( "Scanning band %d, dl_min %"PRIu32", ul_min %"PRIu32"\n", current_band, eutra_bands[ind].dl_min,eutra_bands[ind].ul_min);

      if ((eutra_bands[ind].dl_min <= downlink_frequency[0][0]) && (eutra_bands[ind].dl_max >= downlink_frequency[0][0])) {
        for (card=0; card<MAX_NUM_CCs; card++)
          for (i=0; i<4; i++)
            uplink_frequency_offset[card][i] = eutra_bands[ind].ul_min - eutra_bands[ind].dl_min;

        found = 1;
        break;
      }

      ind++;
    } while (ind < sizeof(eutra_bands) / sizeof(eutra_bands[0]));
  
    if (found == 0) {
      exit_fun("Can't find EUTRA band for frequency");
      return &UE_thread_synch_retval;
    }






    LOG_I( PHY, "[SCHED][UE] Check absolute frequency DL %"PRIu32", UL %"PRIu32" (oai_exit %d)\n", downlink_frequency[0][0], downlink_frequency[0][0]+uplink_frequency_offset[0][0],oai_exit );

    for (i=0;i<openair0_cfg[0].rx_num_channels;i++) {
      openair0_cfg[0].rx_freq[i] = downlink_frequency[0][i];
      openair0_cfg[0].tx_freq[i] = downlink_frequency[0][i]+uplink_frequency_offset[0][i];
      openair0_cfg[0].autocal[i] = 1;
    }

    sync_mode = pbch;

  } else if  (UE->UE_scan == 1) {
    current_band=0;

    for (card=0; card<MAX_CARDS; card++) {
      for (i=0; i<openair0_cfg[card].rx_num_channels; i++) {
        downlink_frequency[card][i] = bands_to_scan.band_info[0].dl_min;
        uplink_frequency_offset[card][i] = bands_to_scan.band_info[0].ul_min-bands_to_scan.band_info[0].dl_min;

        openair0_cfg[card].rx_freq[i] = downlink_frequency[card][i];
        openair0_cfg[card].tx_freq[i] = downlink_frequency[card][i]+uplink_frequency_offset[card][i];
#ifdef OAI_USRP
        openair0_cfg[card].rx_gain[i] = UE->rx_total_gain_dB;//-USRP_GAIN_OFFSET;

#if 0 // UHD 3.8	
        switch(UE->lte_frame_parms.N_RB_DL) {
        case 6:
          openair0_cfg[card].rx_gain[i] -= 12;
          break;

        case 25:
          openair0_cfg[card].rx_gain[i] -= 6;
          break;

        case 50:
          openair0_cfg[card].rx_gain[i] -= 3;
          break;

        case 100:
          openair0_cfg[card].rx_gain[i] -= 0;
          break;

        default:
          printf( "Unknown number of RBs %d\n", UE->lte_frame_parms.N_RB_DL );
          break;
        }
#endif
        printf( "UE synch: setting RX gain (%d,%d) to %f\n", card, i, openair0_cfg[card].rx_gain[i] );
#endif
      }
    }

  }

  while (oai_exit==0) {
  //while ((UE->is_synchronized==0)&& (oai_exit==0)){

    if (pthread_mutex_lock(&UE->mutex_synch) != 0) {
      LOG_E( PHY, "[SCHED][UE] error locking mutex for UE initial synch thread\n" );
      exit_fun("noting to add");
      return &UE_thread_synch_retval;
    }
    

    while (UE->instance_cnt_synch < 0) {
      // the thread waits here most of the time
      pthread_cond_wait( &UE->cond_synch, &UE->mutex_synch );
    }

    if (pthread_mutex_unlock(&UE->mutex_synch) != 0) {
      LOG_E( PHY, "[SCHED][eNB] error unlocking mutex for UE Initial Synch thread\n" );
      exit_fun("nothing to add");
      return &UE_thread_synch_retval;
    }

    VCD_SIGNAL_DUMPER_DUMP_FUNCTION_BY_NAME( VCD_SIGNAL_DUMPER_FUNCTIONS_UE_SYNCH, 1 );

    switch (sync_mode) {
    case pss:
      LOG_I(PHY,"[SCHED][UE] Scanning band %d (%d), freq %u\n",bands_to_scan.band_info[current_band].band, current_band,bands_to_scan.band_info[current_band].dl_min+current_offset);
      lte_sync_timefreq(UE,current_band,bands_to_scan.band_info[current_band].dl_min+current_offset);
      current_offset += 20000000; // increase by 20 MHz

      if (current_offset > bands_to_scan.band_info[current_band].dl_max-bands_to_scan.band_info[current_band].dl_min) {
        current_band++;
        current_offset=0;
      }

      if (current_band==bands_to_scan.nbands) {
        current_band=0;
        oai_exit=1;
      }

      for (card=0; card<MAX_CARDS; card++) {
        for (i=0; i<openair0_cfg[card].rx_num_channels; i++) {
          downlink_frequency[card][i] = bands_to_scan.band_info[current_band].dl_min+current_offset;
          uplink_frequency_offset[card][i] = bands_to_scan.band_info[current_band].ul_min-bands_to_scan.band_info[0].dl_min + current_offset;


          openair0_cfg[card].rx_freq[i] = downlink_frequency[card][i];
          openair0_cfg[card].tx_freq[i] = downlink_frequency[card][i]+uplink_frequency_offset[card][i];
#ifdef OAI_USRP
          openair0_cfg[card].rx_gain[i] = UE->rx_total_gain_dB;//-USRP_GAIN_OFFSET;  // 65 calibrated for USRP B210 @ 2.6 GHz

#if 0 // UHD 3.8	  
          switch(UE->lte_frame_parms.N_RB_DL) {
          case 6:
            openair0_cfg[card].rx_gain[i] -= 12;
            break;

          case 25:
            openair0_cfg[card].rx_gain[i] -= 6;
            break;

          case 50:
            openair0_cfg[card].rx_gain[i] -= 3;
            break;

          case 100:
            openair0_cfg[card].rx_gain[i] -= 0;
            break;

          default:
            printf("Unknown number of RBs %d\n",UE->lte_frame_parms.N_RB_DL);
            break;
          }
#endif	  

          printf("UE synch: setting RX gain (%d,%d) to %f\n",card,i,openair0_cfg[card].rx_gain[i]);
#endif

        }

      }

      if (UE->UE_scan_carrier) {

	for (i=0;i<openair0_cfg[0].rx_num_channels;i++)
	  openair0_cfg[0].autocal[i] = 1;

      }


      break;
 
    case pbch:

      LOG_I(PHY,"[UE thread Synch] Running Initial Synch\n");

      if (initial_sync( UE, UE->mode ) == 0) {

        hw_slot_offset = (UE->rx_offset<<1) / UE->lte_frame_parms.samples_per_tti;
        LOG_I( HW, "Got synch: hw_slot_offset %d\n", hw_slot_offset );
	if (UE->UE_scan_carrier == 1) {

	  UE->UE_scan_carrier = 0;
	  // rerun with new cell parameters and frequency-offset
	  for (i=0;i<openair0_cfg[0].rx_num_channels;i++) {
	    openair0_cfg[0].rx_gain[i] = UE->rx_total_gain_dB;//-USRP_GAIN_OFFSET;
	    openair0_cfg[0].rx_freq[i] -= UE->lte_ue_common_vars.freq_offset;
	    openair0_cfg[0].tx_freq[i] =  openair0_cfg[0].rx_freq[i]+uplink_frequency_offset[0][i];
	    downlink_frequency[0][i] = openair0_cfg[0].rx_freq[i];
	    freq_offset=0;	    
	  }

	  // reconfigure for potentially different bandwidth
	  switch(UE->lte_frame_parms.N_RB_DL) {
	  case 6:
	    openair0_cfg[0].sample_rate =1.92e6;
	    openair0_cfg[0].rx_bw          =.96e6;
	    openair0_cfg[0].tx_bw          =.96e6;
	    //            openair0_cfg[0].rx_gain[0] -= 12;
	    break;
	  case 25:
	    openair0_cfg[0].sample_rate =7.68e6;
	    openair0_cfg[0].rx_bw          =2.5e6;
	    openair0_cfg[0].tx_bw          =2.5e6;
	    //            openair0_cfg[0].rx_gain[0] -= 6;
	    break;
	  case 50:
	    openair0_cfg[0].sample_rate =15.36e6;
	    openair0_cfg[0].rx_bw          =5.0e6;
	    openair0_cfg[0].tx_bw          =5.0e6;
	    //            openair0_cfg[0].rx_gain[0] -= 3;
	    break;
	  case 100:
	    openair0_cfg[0].sample_rate=30.72e6;
	    openair0_cfg[0].rx_bw=10.0e6;
	    openair0_cfg[0].tx_bw=10.0e6;
	    //            openair0_cfg[0].rx_gain[0] -= 0;
	    break;
	  }
#ifndef EXMIMO
	  openair0.trx_set_freq_func(&openair0,&openair0_cfg[0],0);
	  //openair0.trx_set_gains_func(&openair0,&openair0_cfg[0]);
	  //openair0.trx_stop_func(0);	  
#else
	  openair0_set_frequencies(&openair0,&openair0_cfg[0],0);
	  openair0_set_gains(&openair0,&openair0_cfg[0]);
	  openair0_stop(0);
#endif
	  //TaiHM
	  //Waiting for feedback from SDN
	  //Update SDN_flag and eNB_id_SDN here
	  char line[80];
	      	  SDN_file = fopen("SDN.dat","rt"); //Read SDN.dat file to update the eNB ID
	      	    if (SDN_file == NULL)
	      	    {
	      	    	//SDN does not update yet,
	      	    	//oai_exit = 1;
	      	    	//exit_fun("SDN FILE null: SDN not feedback yet!!");
	      	    	exit(1);
	      	    }
	      	    else
	      	    {
	      	    	if(fgets(line, 10, SDN_file) != NULL){
	      	    		sscanf(line,"%d",&SDN_flag);
	      	    		//Check the SDN_flag
	      	    			 if(SDN_flag==1){
	      	    				 if(fgets(line, 10, SDN_file) != NULL){
	      	    					 sscanf(line,"%d",&eNB_id_SDN);
	      	    					 //The UE will connect with the eNB which is selected by SND
	      	    					 //The UE first selects the best eNB by itself, after getting feedback from SND (information of selected eNB)
	      	    					 //The UE then update the eNB (Nid_cell) for the next RRC and NAS connectivity
	      	    					 if(UE->lte_frame_parms.Nid_cell==eNB_id_SDN){
	      	    						  //The eNB selected by SDN is the same with the best one selected by UE
	      	    					 }
	      	    					 else{
	      	    						  //The eNB selected by SDN is different with the one selected by UE
	      	    						  //Update Nid_cell variable then UE could connect to the new eNB
	      	    						  UE->lte_frame_parms.Nid_cell=eNB_id_SDN;
	      	    					 }
	      	    				 }
	      	    				 else{
	      	    					 // No Cell id found
	      	    					 //oai_exit = 1;
	      	    					 //exit_fun("No data found: SDN not feedback yet!!");
	      	    					exit(1);
	      	    				 }
	      	    			 }
	      	    			 else{
	      	    				 // SDN_flag not update yet
	      	    				//oai_exit = 1;
	      	    				//exit_fun("SDN_flag not update yet: SDN not feedback yet!!");
	      	    				exit(1);
	      	    			 }
	      	    		}

	      	    	fclose(SDN_file);
	      	    }

	      //UE->lte_frame_parms.Nid_cell=eNB_id_SDN;

	  sleep(1);
	  init_frame_parms(&UE->lte_frame_parms,1);
	}
	else {
	  UE->is_synchronized = 1;

	 if( UE->mode == rx_dump_frame ){
	   FILE *fd;
	   if ((UE->frame_rx&1) == 0) {  // this guarantees SIB1 is present 
	     if ((fd = fopen("rxsig_frame0.dat","w")) != NULL) {
	       fwrite((void*)&UE->lte_ue_common_vars.rxdata[0][0],
		      sizeof(int32_t),
		      10*UE->lte_frame_parms.samples_per_tti,
		      fd);
	       LOG_I(PHY,"Dummping Frame ... bye bye \n");
	       fclose(fd);
	       //exit(0);
	       //UE->is_synchronized = 0;
	     }
	     else {
	       LOG_E(PHY,"Cannot open file for writing\n");
	       //exit(0);
	       //UE->is_synchronized = 0;
	     }
	   }
	   else {
	     UE->is_synchronized = 0;
	   }
	 }
	 

#ifndef EXMIMO
	  UE->slot_rx = 0;
	  UE->slot_tx = 4;
#else
	  UE->slot_rx = 18;
	  UE->slot_tx = 2;
#endif
	}
      } else {
        // initial sync failed
        // calculate new offset and try again
	if (UE->UE_scan_carrier == 1) {
	  if (freq_offset >= 0) {
	    freq_offset += 100;
	    freq_offset *= -1;
	  } else {
	    freq_offset *= -1;
	  }
	
	  if (abs(freq_offset) > 7500) {
	    LOG_I( PHY, "[initial_sync] No cell synchronization found, abandoning\n" );
	    FILE *fd;
	    if ((fd = fopen("rxsig_frame0.dat","w"))!=NULL) {
	      fwrite((void*)&UE->lte_ue_common_vars.rxdata[0][0],
		     sizeof(int32_t),
		     10*UE->lte_frame_parms.samples_per_tti,
		     fd);
	      LOG_I(PHY,"Dummping Frame ... \n");
	      fclose(fd);
	      //exit(0);
	      UE->is_synchronized = 0;
	      LOG_I(PHY,"[TAIHM] Repeat Synch ... \n");
	    }
	    //mac_xface->macphy_exit("No cell synchronization found, abandoning");
	    //return &UE_thread_synch_retval; // not reached
	    UE->is_synchronized = 0;
	  }
	}
	else {
	  
	}
        LOG_I( PHY, "[initial_sync] trying carrier off %d Hz, rxgain %d (DL %u, UL %u)\n", 
	       freq_offset,
               UE->rx_total_gain_dB,
               downlink_frequency[0][0]+freq_offset,
               downlink_frequency[0][0]+uplink_frequency_offset[0][0]+freq_offset );

        for (card=0; card<MAX_CARDS; card++) {
          for (i=0; i<openair0_cfg[card].rx_num_channels; i++) {
            openair0_cfg[card].rx_freq[i] = downlink_frequency[card][i]+freq_offset;
            openair0_cfg[card].tx_freq[i] = downlink_frequency[card][i]+uplink_frequency_offset[card][i]+freq_offset;
#ifndef EXMIMO
	    openair0.trx_set_freq_func(&openair0,&openair0_cfg[0],0);
	    
#else
	    openair0_set_frequencies(&openair0,&openair0_cfg[0],0);
	    
#endif

#if defined(OAI_USRP) || defined(OAI_BLADERF) || defined(OAI_LMSSDR)
            openair0_cfg[card].rx_gain[i] = UE->rx_total_gain_dB;//-USRP_GAIN_OFFSET;
	    
	    
#if 0
            switch(UE->lte_frame_parms.N_RB_DL) {
            case 6:
              openair0_cfg[card].rx_gain[i] -= 12;
              break;

            case 25:
              openair0_cfg[card].rx_gain[i] -= 6;
              break;

            case 50:
              openair0_cfg[card].rx_gain[i] -= 0;//3;
              break;

            case 100:
              openair0_cfg[card].rx_gain[i] -= 0;
              break;

            default:
              printf("Unknown number of RBs %d\n",UE->lte_frame_parms.N_RB_DL);
              break;
            }
#endif	    
#endif
          }
        }
	if (UE->UE_scan_carrier==1) {
	  for (i=0;i<openair0_cfg[0].rx_num_channels;i++)
	    openair0_cfg[0].autocal[i] = 1;
	  
	}
      }// initial_sync=0

      break;

    case si:
    default:
      break;
    }

    VCD_SIGNAL_DUMPER_DUMP_FUNCTION_BY_NAME( VCD_SIGNAL_DUMPER_FUNCTIONS_UE_SYNCH, 0 );



    if (pthread_mutex_lock(&UE->mutex_synch) != 0) {
      LOG_E( PHY, "[SCHED][UE] error locking mutex for UE synch\n" );
      exit_fun("noting to add");
      return &UE_thread_synch_retval;
    }

    // indicate readiness
    UE->instance_cnt_synch--;

    if (pthread_mutex_unlock(&UE->mutex_synch) != 0) {
      LOG_E( PHY, "[SCHED][UE] error unlocking mutex for UE synch\n" );
      exit_fun("noting to add");
      return &UE_thread_synch_retval;
    }

    VCD_SIGNAL_DUMPER_DUMP_FUNCTION_BY_NAME( VCD_SIGNAL_DUMPER_FUNCTIONS_UE_SYNCH, 0 );
  }  // while !oai_exit

  return &UE_thread_synch_retval;
}














Appendix Q: 
Read the information from USRP :
In lte_ue_measurement.c:
/*******************************************************************************
    OpenAirInterface
    Copyright(c) 1999 - 2014 Eurecom

    OpenAirInterface is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.


    OpenAirInterface is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with OpenAirInterface.The full GNU General Public License is
   included in this distribution in the file called "COPYING". If not,
   see <http://www.gnu.org/licenses/>.

  Contact Information
  OpenAirInterface Admin: openair_admin@eurecom.fr
  OpenAirInterface Tech : openair_tech@eurecom.fr
  OpenAirInterface Dev  : openair4g-devel@lists.eurecom.fr

  Address      : Eurecom, Campus SophiaTech, 450 Route des Chappes, CS 50193 - 06904 Biot Sophia Antipolis cedex, FRANCE

 *******************************************************************************/
// this function fills the PHY_vars->PHY_measurement structure

#include "PHY/defs.h"
#include "PHY/extern.h"
#include "SCHED/defs.h"
#include "SCHED/extern.h"
#include "log.h"
#include "PHY/sse_intrin.h"
//#include <iostream>
//#include <fstream>
//#include <string>
//#include <vector>

//#define k1 1000
#define k1 ((long long int) 1000)
#define k2 ((long long int) (1024-k1))

//#define DEBUG_MEAS

#ifdef USER_MODE
void print_shorts(char *s,short *x)
{


  printf("%s  : %d,%d,%d,%d,%d,%d,%d,%d\n",s,
         x[0],x[1],x[2],x[3],x[4],x[5],x[6],x[7]
        );

}
void print_ints(char *s,int *x)
{


  printf("%s  : %d,%d,%d,%d\n",s,
         x[0],x[1],x[2],x[3]
        );

}
#endif


int16_t get_PL(uint8_t Mod_id,uint8_t CC_id,uint8_t eNB_index)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];
  /*
  int RSoffset;


  if (phy_vars_ue->lte_frame_parms.mode1_flag == 1)
    RSoffset = 6;
  else
    RSoffset = 3;
  */

  LOG_D(PHY,"get_PL : Frame %d : rsrp %f dBm/RE (%f), eNB power %d dBm/RE\n", phy_vars_ue->frame_rx,
        (1.0*dB_fixed_times10(phy_vars_ue->PHY_measurements.rsrp[eNB_index])-(10.0*phy_vars_ue->rx_total_gain_dB))/10.0,
        10*log10((double)phy_vars_ue->PHY_measurements.rsrp[eNB_index]),
        phy_vars_ue->lte_frame_parms.pdsch_config_common.referenceSignalPower);

  return((int16_t)(((10*phy_vars_ue->rx_total_gain_dB) -
                    dB_fixed_times10(phy_vars_ue->PHY_measurements.rsrp[eNB_index])+
                    //        dB_fixed_times10(RSoffset*12*PHY_vars_UE_g[Mod_id][CC_id]->lte_frame_parms.N_RB_DL) +
                    (phy_vars_ue->lte_frame_parms.pdsch_config_common.referenceSignalPower*10))/10));
}


uint8_t get_n_adj_cells (uint8_t Mod_id,uint8_t CC_id)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue)
    return phy_vars_ue->PHY_measurements.n_adj_cells;
  else
    return 0;
}

uint32_t get_rx_total_gain_dB (uint8_t Mod_id,uint8_t CC_id)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue)
    return phy_vars_ue->rx_total_gain_dB;

  return 0xFFFFFFFF;
}
uint32_t get_RSSI (uint8_t Mod_id,uint8_t CC_id)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue)
    return phy_vars_ue->PHY_measurements.rssi;

  return 0xFFFFFFFF;
}
uint32_t get_RSRP(uint8_t Mod_id,uint8_t CC_id,uint8_t eNB_index)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue)
    return phy_vars_ue->PHY_measurements.rsrp[eNB_index];

  return 0xFFFFFFFF;
}

uint32_t get_RSRQ(uint8_t Mod_id,uint8_t CC_id,uint8_t eNB_index)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue)
    return phy_vars_ue->PHY_measurements.rsrq[eNB_index];

  return 0xFFFFFFFF;
}

int8_t set_RSRP_filtered(uint8_t Mod_id,uint8_t CC_id,uint8_t eNB_index,float rsrp)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue) {
    phy_vars_ue->PHY_measurements.rsrp_filtered[eNB_index]=rsrp;
    return 0;
  }

  LOG_W(PHY,"[UE%d] could not set the rsrp\n",Mod_id);
  return -1;
}

int8_t set_RSRQ_filtered(uint8_t Mod_id,uint8_t CC_id,uint8_t eNB_index,float rsrq)
{

  PHY_VARS_UE *phy_vars_ue = PHY_vars_UE_g[Mod_id][CC_id];

  if (phy_vars_ue) {
    phy_vars_ue->PHY_measurements.rsrq_filtered[eNB_index]=rsrq;
    return 0;
  }

  LOG_W(PHY,"[UE%d] could not set the rsrq\n",Mod_id);
  return -1;

}

void ue_rrc_measurements(PHY_VARS_UE *phy_vars_ue,
                         uint8_t slot,
                         uint8_t abstraction_flag)
{

  int aarx,rb;
  int16_t *rxF,*rxF_pss,*rxF_sss;

  uint16_t Nid_cell = phy_vars_ue->lte_frame_parms.Nid_cell;
  uint8_t eNB_offset,nu,l,nushift,k;
  uint16_t off;

  //phy_vars_ue->PHY_measurements.n_adj_cells = 2;//TAIHM
  //LOG_I(PHY,"[TAIHM7][UE%d] n_adj_cells %d \n",phy_vars_ue->Mod_id,phy_vars_ue->PHY_measurements.n_adj_cells);

  for (eNB_offset = 0; eNB_offset<1+phy_vars_ue->PHY_measurements.n_adj_cells; eNB_offset++) {

	  //LOG_I(PHY,"[TAIHM7][UE%d] eNB_offset: %d\n",phy_vars_ue->Mod_id,eNB_offset);
    if (eNB_offset==0) {
      phy_vars_ue->PHY_measurements.rssi = 0;
      phy_vars_ue->PHY_measurements.n0_power_tot = 0;

      if (abstraction_flag == 0) {
        if ((phy_vars_ue->lte_frame_parms.frame_type == FDD) &&
            ((slot == 0) || (slot == 10))) {  // FDD PSS/SSS, compute noise in DTX REs

          if (phy_vars_ue->lte_frame_parms.Ncp==NORMAL) {
            for (aarx=0; aarx<phy_vars_ue->lte_frame_parms.nb_antennas_rx; aarx++) {

	      rxF_sss = (int16_t *)&phy_vars_ue->lte_ue_common_vars.rxdataF[aarx][(5*phy_vars_ue->lte_frame_parms.ofdm_symbol_size)];
	      rxF_pss = (int16_t *)&phy_vars_ue->lte_ue_common_vars.rxdataF[aarx][(6*phy_vars_ue->lte_frame_parms.ofdm_symbol_size)];
	      

              //-ve spectrum from SSS
	      //	      printf("slot %d: SSS DTX: %d,%d, non-DTX %d,%d\n",slot,rxF_pss[-72],rxF_pss[-71],rxF_pss[-36],rxF_pss[-35]);

	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] = (((int32_t)rxF_pss[-72]*rxF_pss[-72])+((int32_t)rxF_pss[-71]*rxF_pss[-71]));
	      //	      printf("sssn36 %d\n",phy_vars_ue->PHY_measurements.n0_power[aarx]);
              phy_vars_ue->PHY_measurements.n0_power[aarx] = (((int32_t)rxF_pss[-70]*rxF_pss[-70])+((int32_t)rxF_pss[-69]*rxF_pss[-69]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-68]*rxF_pss[-68])+((int32_t)rxF_pss[-67]*rxF_pss[-67]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-66]*rxF_pss[-66])+((int32_t)rxF_pss[-65]*rxF_pss[-65]));
	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-64]*rxF_pss[-64])+((int32_t)rxF_pss[-63]*rxF_pss[-63]));
	      //	      printf("sssm32 %d\n",phy_vars_ue->PHY_measurements.n0_power[aarx]);
              //+ve spectrum from SSS
	      phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+70]*rxF_sss[2+70])+((int32_t)rxF_sss[2+69]*rxF_sss[2+69]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+68]*rxF_sss[2+68])+((int32_t)rxF_sss[2+67]*rxF_sss[2+67]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+66]*rxF_sss[2+66])+((int32_t)rxF_sss[2+65]*rxF_sss[2+65]));
	      //	      phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+64]*rxF_sss[2+64])+((int32_t)rxF_sss[2+63]*rxF_sss[2+63]));
	      //	      printf("sssp32 %d\n",phy_vars_ue->PHY_measurements.n0_power[aarx]);
              //+ve spectrum from PSS
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[2+70]*rxF_pss[2+70])+((int32_t)rxF_pss[2+69]*rxF_pss[2+69]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[2+68]*rxF_pss[2+68])+((int32_t)rxF_pss[2+67]*rxF_pss[2+67]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[2+66]*rxF_pss[2+66])+((int32_t)rxF_pss[2+65]*rxF_pss[2+65]));
	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[2+64]*rxF_pss[2+64])+((int32_t)rxF_pss[2+63]*rxF_pss[2+63]));
	      //	      printf("pss32 %d\n",phy_vars_ue->PHY_measurements.n0_power[aarx]);              //-ve spectrum from PSS
              rxF_pss = (int16_t *)&phy_vars_ue->lte_ue_common_vars.rxdataF[aarx][(7*phy_vars_ue->lte_frame_parms.ofdm_symbol_size)];
	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-72]*rxF_pss[-72])+((int32_t)rxF_pss[-71]*rxF_pss[-71]));
	      //	      printf("pssm36 %d\n",phy_vars_ue->PHY_measurements.n0_power[aarx]);
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-70]*rxF_pss[-70])+((int32_t)rxF_pss[-69]*rxF_pss[-69]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-68]*rxF_pss[-68])+((int32_t)rxF_pss[-67]*rxF_pss[-67]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-66]*rxF_pss[-66])+((int32_t)rxF_pss[-65]*rxF_pss[-65]));
	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-64]*rxF_pss[-64])+((int32_t)rxF_pss[-63]*rxF_pss[-63]));
	      //	      printf("pssm32 %d\n",phy_vars_ue->PHY_measurements.n0_power[aarx]);
              phy_vars_ue->PHY_measurements.n0_power_dB[aarx] = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.n0_power[aarx]/12);
              phy_vars_ue->PHY_measurements.n0_power_tot +=  phy_vars_ue->PHY_measurements.n0_power[aarx];
            }

	    phy_vars_ue->PHY_measurements.n0_power_tot_dB = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.n0_power_tot/(12*aarx));
	    phy_vars_ue->PHY_measurements.n0_power_tot_dBm = phy_vars_ue->PHY_measurements.n0_power_tot_dB - phy_vars_ue->rx_total_gain_dB - dB_fixed(phy_vars_ue->lte_frame_parms.ofdm_symbol_size);
	  }
        }
	else if ((phy_vars_ue->lte_frame_parms.frame_type == TDD) &&
		 (slot == 1)) {  // TDD SSS, compute noise in DTX REs

          if (phy_vars_ue->lte_frame_parms.Ncp==NORMAL) {
            for (aarx=0; aarx<phy_vars_ue->lte_frame_parms.nb_antennas_rx; aarx++) {

	      rxF_sss = (int16_t *)&phy_vars_ue->lte_ue_common_vars.rxdataF[aarx][(6*phy_vars_ue->lte_frame_parms.ofdm_symbol_size)];
	      // note this is a dummy pointer, the pss is not really there!
	      // in FDD the pss is in the symbol after the sss, but not in TDD
	      rxF_pss = (int16_t *)&phy_vars_ue->lte_ue_common_vars.rxdataF[aarx][(7*phy_vars_ue->lte_frame_parms.ofdm_symbol_size)];
	      
	      //-ve spectrum from SSS
	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] = (((int32_t)rxF_pss[-72]*rxF_pss[-72])+((int32_t)rxF_pss[-71]*rxF_pss[-71]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] = (((int32_t)rxF_pss[-70]*rxF_pss[-70])+((int32_t)rxF_pss[-69]*rxF_pss[-69]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-68]*rxF_pss[-68])+((int32_t)rxF_pss[-67]*rxF_pss[-67]));
              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-66]*rxF_pss[-66])+((int32_t)rxF_pss[-65]*rxF_pss[-65]));
	      //              phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_pss[-64]*rxF_pss[-64])+((int32_t)rxF_pss[-63]*rxF_pss[-63]));
	      //+ve spectrum from SSS
	      //	      phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+72]*rxF_sss[2+72])+((int32_t)rxF_sss[2+71]*rxF_sss[2+71]));
	      phy_vars_ue->PHY_measurements.n0_power[aarx] = (((int32_t)rxF_sss[2+70]*rxF_sss[2+70])+((int32_t)rxF_sss[2+69]*rxF_sss[2+69]));
	      phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+68]*rxF_sss[2+68])+((int32_t)rxF_sss[2+67]*rxF_sss[2+67]));
	      phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+66]*rxF_sss[2+66])+((int32_t)rxF_sss[2+65]*rxF_sss[2+65]));
	      //	      phy_vars_ue->PHY_measurements.n0_power[aarx] += (((int32_t)rxF_sss[2+64]*rxF_sss[2+64])+((int32_t)rxF_sss[2+63]*rxF_sss[2+63]));
	      
	      phy_vars_ue->PHY_measurements.n0_power_dB[aarx] = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.n0_power[aarx]/(6));
	      phy_vars_ue->PHY_measurements.n0_power_tot +=  phy_vars_ue->PHY_measurements.n0_power[aarx];	  
	    }	      
	    phy_vars_ue->PHY_measurements.n0_power_tot_dB = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.n0_power_tot/(6*aarx));
	    phy_vars_ue->PHY_measurements.n0_power_tot_dBm = phy_vars_ue->PHY_measurements.n0_power_tot_dB - phy_vars_ue->rx_total_gain_dB - dB_fixed(phy_vars_ue->lte_frame_parms.ofdm_symbol_size);
	      
	    
	  }
	}
      }
    }
    // recompute nushift with eNB_offset corresponding to adjacent eNB on which to perform channel estimation
    //    printf("[PHY][UE %d] Frame %d slot %d Doing ue_rrc_measurements rsrp/rssi (Nid_cell %d, Nid2 %d, nushift %d, eNB_offset %d)\n",phy_vars_ue->Mod_id,phy_vars_ue->frame,slot,Nid_cell,Nid2,nushift,eNB_offset);
    if (eNB_offset > 0)
      Nid_cell = phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1];


    nushift =  Nid_cell%6;



    phy_vars_ue->PHY_measurements.rsrp[eNB_offset] = 0;


    if (abstraction_flag == 0) {

      // compute RSRP using symbols 0 and 4-frame_parms->Ncp

      for (l=0,nu=0; l<=(4-phy_vars_ue->lte_frame_parms.Ncp); l+=(4-phy_vars_ue->lte_frame_parms.Ncp),nu=3) {
        k = (nu + nushift)%6;
#ifdef DEBUG_MEAS
        LOG_I(PHY,"[UE %d] Frame %d slot %d Doing ue_rrc_measurements rsrp/rssi (Nid_cell %d, nushift %d, eNB_offset %d, k %d, l %d)\n",phy_vars_ue->Mod_id,phy_vars_ue->frame_rx,slot,Nid_cell,nushift,
              eNB_offset,k,l);
#endif

        for (aarx=0; aarx<phy_vars_ue->lte_frame_parms.nb_antennas_rx; aarx++) {
          rxF = (int16_t *)&phy_vars_ue->lte_ue_common_vars.rxdataF[aarx][(l*phy_vars_ue->lte_frame_parms.ofdm_symbol_size)];
          off  = (phy_vars_ue->lte_frame_parms.first_carrier_offset+k)<<1;

          if (l==(4-phy_vars_ue->lte_frame_parms.Ncp)) {
            for (rb=0; rb<phy_vars_ue->lte_frame_parms.N_RB_DL; rb++) {

              //    printf("rb %d, off %d, off2 %d\n",rb,off,off2);

              phy_vars_ue->PHY_measurements.rsrp[eNB_offset] += (((int32_t)(rxF[off])*rxF[off])+((int32_t)(rxF[off+1])*rxF[off+1]));
              //        printf("rb %d, off %d : %d\n",rb,off,((((int32_t)rxF[off])*rxF[off])+((int32_t)(rxF[off+1])*rxF[off+1])));
	      //	      if ((phy_vars_ue->frame_rx&0x3ff) == 0)
	      //                printf("rb %d, off %d : %d\n",rb,off,((rxF[off]*rxF[off])+(rxF[off+1]*rxF[off+1])));

              
              off+=12;

              if (off>=(phy_vars_ue->lte_frame_parms.ofdm_symbol_size<<1))
                off = (1+k)<<1;

              phy_vars_ue->PHY_measurements.rsrp[eNB_offset] += (((int32_t)(rxF[off])*rxF[off])+((int32_t)(rxF[off+1])*rxF[off+1]));
              //    printf("rb %d, off %d : %d\n",rb,off,(((int32_t)(rxF[off])*rxF[off])+((int32_t)(rxF[off+1])*rxF[off+1])));
              /*
                if ((phy_vars_ue->frame_rx&0x3ff) == 0)
                printf("rb %d, off %d : %d\n",rb,off,((rxF[off]*rxF[off])+(rxF[off+1]*rxF[off+1])));
              */
              off+=12;

              if (off>=(phy_vars_ue->lte_frame_parms.ofdm_symbol_size<<1))
                off = (1+k)<<1;

            }

            /*
            if ((eNB_offset==0)&&(l==0)) {
            for (i=0;i<6;i++,off2+=4)
            phy_vars_ue->PHY_measurements.rssi += ((rxF[off2]*rxF[off2])+(rxF[off2+1]*rxF[off2+1]));
            if (off2==(phy_vars_ue->lte_frame_parms.ofdm_symbol_size<<2))
            off2=4;
            for (i=0;i<6;i++,off2+=4)
            phy_vars_ue->PHY_measurements.rssi += ((rxF[off2]*rxF[off2])+(rxF[off2+1]*rxF[off2+1]));
            }
            */
            //    printf("slot %d, rb %d => rsrp %d, rssi %d\n",slot,rb,phy_vars_ue->PHY_measurements.rsrp[eNB_offset],phy_vars_ue->PHY_measurements.rssi);
          }
        }
      }

      // 2 RE per PRB
      //      phy_vars_ue->PHY_measurements.rsrp[eNB_offset]/=(24*phy_vars_ue->lte_frame_parms.N_RB_DL);
      phy_vars_ue->PHY_measurements.rsrp[eNB_offset]/=(2*phy_vars_ue->lte_frame_parms.N_RB_DL*phy_vars_ue->lte_frame_parms.ofdm_symbol_size);

            LOG_I(PHY,"[TAIHM7]eNB: %d, RSRP: %3.1f \n",(eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell,10*log10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])-phy_vars_ue->rx_total_gain_dB);

            LOG_I(PHY,"[TAIHM8][UE %d] (TRA) Frame %d, slot %d RRC Measurements (idx %d, Cell id %d) => rsrp: %3.1f dBm/RE (%d), rsrq: %3.1f dB\n",
                        phy_vars_ue->Mod_id,
                        phy_vars_ue->frame_rx,slot,eNB_offset,
                        (eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell,
                        10*log10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])-phy_vars_ue->rx_total_gain_dB,
                        phy_vars_ue->PHY_measurements.rsrp[eNB_offset],
                        (10*log10(phy_vars_ue->PHY_measurements.rsrq[eNB_offset])));
            //TRA ADD
             int j=0;
             int a;
             int b;
             int c;
                float numberArray[45]={0};
            	    int i;
            	 FILE *myFile;
            	    myFile = fopen("/home/ue/openairinterface5g/openair1/PHY/LTE_ESTIMATION/data.txt", "r");
            	    //int no_lines=0;
            	    //read file into array


            	    if (myFile == NULL)
            	    {
            	        printf("Error Reading File\n");
            	        exit (0);
            	    }

            	    for (i = 0; i < 45; i++)
            	    {
            	        fscanf(myFile, "%f", &numberArray[i] );

            	    }
            	    fclose(myFile);
            	    /*for (i = 0; i < 15; i++)
            	    {
            	           printf("Number is: %3.1f\n\n", numberArray[i]);
            	       }*/


            	    b=0;
            	              	    for( j=0;j<45;j++)
            	              	       {
            	              	    	    b++;
            	              	        	if(numberArray[j]==0)
            	              	        	{
            	              	        		break;
            	              	        	}

            	              	        }
                  //printf("length=%d",b);

                  //LOG_I(PHY,"length=%d\n",b);

            	              	  j=0;
            	              	             	                  a=0;
            	              	             	                  while(j<45)

            	              	             	                  {
            	              	             	                      	int n= (int) numberArray[j];
            	              	             	                      	//LOG_I(PHY,"value of eNB %d\n",n);
            	              	             	                      	c=(eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell;
            	              	             	                      	//LOG_I(PHY,"value of eNB moi %d\n",(eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell);
            	              	             	                      	if(n==c)
            	              	             	                      	{
            	              	             	                      		a=1;
            	              	             	                      		break;
            	              	             	                      		//fprintf(fp,"%0.2f\n",7.00);

            	              	             	                      	}
            	              	             	                      	j=j+3;

            	              	             	                   }
            	              	             	                 /*LOG_I(PHY,"a=%d\n",a);
            	              	             	                  for(j=0;j<45;j++)
            	              	             	                  {
            	              	             	                              	                	  LOG_I(PHY,"array value: %3.1f\n",numberArray[j]);
            	              	             	                              	                  }*/
            	              	             	               if(a==0)
            	              	             	               {
            	              	             	            	   numberArray[b-1]=(float)(eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell;
            	              	             	            	   numberArray[b]=10*log10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])-phy_vars_ue->rx_total_gain_dB;
            	              	             	            	   numberArray[b+1]=(10*log10(phy_vars_ue->PHY_measurements.rsrq[eNB_offset]));
            	              	             	                  FILE *fp=fopen ("/home/ue/openairinterface5g/openair1/PHY/LTE_ESTIMATION/data.txt", "w");
            	              	             	                  for(j=0;j<45;j++)
            	              	             	                  {
            	              	             	                	  if(j%3==2)
            	              	             	                	  {
            	              	             	                		fprintf(fp,"%3.1f\n ",numberArray[j]);
            	              	             	                	  }
            	              	             	                	  else
            	              	             	                	  {
            	              	             	                	  fprintf(fp,"%3.1f ",numberArray[j]);
            	              	             	                	  }
            	              	             	                	  
            	              	             	                  }
            	              	             	fclose(fp);}


            //
      if (eNB_offset == 0) {
        //  phy_vars_ue->PHY_measurements.rssi/=(24*phy_vars_ue->lte_frame_parms.N_RB_DL);
        //  phy_vars_ue->PHY_measurements.rssi*=rx_power_correction;
        //  phy_vars_ue->PHY_measurements.rssi=phy_vars_ue->PHY_measurements.rsrp[0]*24/2;
        phy_vars_ue->PHY_measurements.rssi=phy_vars_ue->PHY_measurements.rsrp[0]*(12*phy_vars_ue->lte_frame_parms.N_RB_DL);
      }

      if (phy_vars_ue->PHY_measurements.rssi>0)
      {
        phy_vars_ue->PHY_measurements.rsrq[eNB_offset] = 100*phy_vars_ue->PHY_measurements.rsrp[eNB_offset]*phy_vars_ue->lte_frame_parms.N_RB_DL/phy_vars_ue->PHY_measurements.rssi;
        //LOG_I(PHY,"[TAIHM2]eNB: %d, RSRQ: %3.1f \n",eNB_offset,phy_vars_ue->PHY_measurements.rsrq[eNB_offset]);
      }
      else
        phy_vars_ue->PHY_measurements.rsrq[eNB_offset] = -12000;

      //((200*phy_vars_ue->PHY_measurements.rsrq[eNB_offset]) + ((1024-200)*100*phy_vars_ue->PHY_measurements.rsrp[eNB_offset]*phy_vars_ue->lte_frame_parms.N_RB_DL/phy_vars_ue->PHY_measurements.rssi))>>10;
    } else { // Do abstraction of RSRP and RSRQ
      phy_vars_ue->PHY_measurements.rssi = phy_vars_ue->PHY_measurements.rx_power_avg[0];
      // dummay value for the moment
      phy_vars_ue->PHY_measurements.rsrp[eNB_offset] = -93 ;
      phy_vars_ue->PHY_measurements.rsrq[eNB_offset] = 3;

    }

#ifdef DEBUG_MEAS

    //    if (slot == 0) {

      if (eNB_offset == 0)
        LOG_I(PHY,"[UE %d] Frame %d, slot %d RRC Measurements => rssi %3.1f dBm (digital: %3.1f dB, gain %d), N0 %d dBm\n",phy_vars_ue->Mod_id,
              phy_vars_ue->frame_rx,slot,10*log10(phy_vars_ue->PHY_measurements.rssi)-phy_vars_ue->rx_total_gain_dB,
              10*log10(phy_vars_ue->PHY_measurements.rssi),
              phy_vars_ue->rx_total_gain_dB,
              phy_vars_ue->PHY_measurements.n0_power_tot_dBm);

            LOG_I(PHY,"[UE %d] Frame %d, slot %d RRC Measurements (idx %d, Cell id %d) => rsrp: %3.1f dBm/RE (%d), rsrq: %3.1f dB\n",             phy_vars_ue->Mod_id,             phy_vars_ue->frame_rx,slot,eNB_offset,             (eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell,             10*log10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])-phy_vars_ue->rx_total_gain_dB,             phy_vars_ue->PHY_measurements.rsrp[eNB_offset],             (10*log10(phy_vars_ue->PHY_measurements.rsrq[eNB_offset])));
 LOG_I(PHY,"TRA [UE %d] Frame %d, slot %d RRC Measurements (idx %d, Cell id %d) => rsrp: %3.1f dBm/RE (%d), rsrq: %3.1f dB\n",             phy_vars_ue->Mod_id,             phy_vars_ue->frame_rx,slot,eNB_offset,             (eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell,             10*log10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])-phy_vars_ue->rx_total_gain_dB,             phy_vars_ue->PHY_measurements.rsrp[eNB_offset],             (10*log10(phy_vars_ue->PHY_measurements.rsrq[eNB_offset])));

      //LOG_D(PHY,"RSRP_total_dB: %3.2f \n",(dB_fixed_times10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])/10.0)-phy_vars_ue->rx_total_gain_dB-dB_fixed(phy_vars_ue->lte_frame_parms.N_RB_DL*12));

      //LOG_D(PHY,"RSRP_dB: %3.2f \n",(dB_fixed_times10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])/10.0));
      //LOG_D(PHY,"gain_loss_dB: %d \n",phy_vars_ue->rx_total_gain_dB);
      //LOG_D(PHY,"gain_fixed_dB: %d \n",dB_fixed(phy_vars_ue->lte_frame_parms.N_RB_DL*12));

      //    }

#endif
  }

}

void lte_ue_measurements(PHY_VARS_UE *phy_vars_ue,
                         unsigned int subframe_offset,
                         unsigned char N0_symbol,
                         unsigned char abstraction_flag)
{


  int aarx,aatx,eNB_id=0; //TAIHM set connected eNB to be 1
  //,gain_offset=0;
  //int rx_power[NUMBER_OF_CONNECTED_eNB_MAX];
  int i;
  unsigned int limit,subband;
#if defined(__x86_64__) || defined(__i386__)
  __m128i *dl_ch0_128,*dl_ch1_128;
#elif defined(__arm__)
  int16x8_t *dl_ch0_128, *dl_ch1_128;
#endif
  int *dl_ch0,*dl_ch1;
  LTE_DL_FRAME_PARMS *frame_parms = &phy_vars_ue->lte_frame_parms;
  int nb_subbands,subband_size,last_subband_size;
  int N_RB_DL = frame_parms->N_RB_DL;

  switch (N_RB_DL) {
  case 6:
    nb_subbands = 6;
    subband_size = 12;
    last_subband_size = 0;
    break;

  default:
  case 25:
    nb_subbands = 7;
    subband_size = 4*12;
    last_subband_size = 12;
    break;

  case 50:
    nb_subbands = 9;
    subband_size = 6*12;
    last_subband_size = 2*12;
    break;

  case 100:
    nb_subbands = 13;
    subband_size = 8*12;
    last_subband_size = 4*12;
    break;
  }
LOG_I(PHY,"TRA [UE %d] eNB %d can be seen  \n", phy_vars_ue->Mod_id, phy_vars_ue->n_connected_eNB);
  // signal measurements
  for (eNB_id=0; eNB_id<phy_vars_ue->n_connected_eNB; eNB_id++) {
    for (aarx=0; aarx<frame_parms->nb_antennas_rx; aarx++) {
      for (aatx=0; aatx<frame_parms->nb_antennas_tx_eNB; aatx++) {
        phy_vars_ue->PHY_measurements.rx_spatial_power[eNB_id][aatx][aarx] =
          (signal_energy_nodc(&phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][(aatx<<1) + aarx][0],
                              (N_RB_DL*12)));
        //- phy_vars_ue->PHY_measurements.n0_power[aarx];

        if (phy_vars_ue->PHY_measurements.rx_spatial_power[eNB_id][aatx][aarx]<0)
          phy_vars_ue->PHY_measurements.rx_spatial_power[eNB_id][aatx][aarx] = 0; //phy_vars_ue->PHY_measurements.n0_power[aarx];

        phy_vars_ue->PHY_measurements.rx_spatial_power_dB[eNB_id][aatx][aarx] = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.rx_spatial_power[eNB_id][aatx][aarx]);

        if (aatx==0)
          phy_vars_ue->PHY_measurements.rx_power[eNB_id][aarx] = phy_vars_ue->PHY_measurements.rx_spatial_power[eNB_id][aatx][aarx];
        else
          phy_vars_ue->PHY_measurements.rx_power[eNB_id][aarx] += phy_vars_ue->PHY_measurements.rx_spatial_power[eNB_id][aatx][aarx];
      } //aatx

      phy_vars_ue->PHY_measurements.rx_power_dB[eNB_id][aarx] = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.rx_power[eNB_id][aarx]);

      if (aarx==0)
        phy_vars_ue->PHY_measurements.rx_power_tot[eNB_id] = phy_vars_ue->PHY_measurements.rx_power[eNB_id][aarx];
      else
        phy_vars_ue->PHY_measurements.rx_power_tot[eNB_id] += phy_vars_ue->PHY_measurements.rx_power[eNB_id][aarx];
    } //aarx

    phy_vars_ue->PHY_measurements.rx_power_tot_dB[eNB_id] = (unsigned short) dB_fixed(phy_vars_ue->PHY_measurements.rx_power_tot[eNB_id]);
//LOG_I(PHY,"TRA [UE %d] Frame %d, slot %d RRC Measurements (idx %d, Cell id %d) => rsrp: %3.1f dBm/RE (%d), rsrq: %3.1f dB\n",             phy_vars_ue->Mod_id,             phy_vars_ue->frame_rx,slot,eNB_offset,             (eNB_offset>0) ? phy_vars_ue->PHY_measurements.adj_cell_id[eNB_offset-1] : phy_vars_ue->lte_frame_parms.Nid_cell,             10*log10(phy_vars_ue->PHY_measurements.rsrp[eNB_offset])-phy_vars_ue->rx_total_gain_dB,             phy_vars_ue->PHY_measurements.rsrp[eNB_offset],             (10*log10(phy_vars_ue->PHY_measurements.rsrq[eNB_offset])));
  } //eNB_id

  // filter to remove jitter
  if (phy_vars_ue->init_averaging == 0) {
    for (eNB_id = 0; eNB_id < phy_vars_ue->n_connected_eNB; eNB_id++)
      phy_vars_ue->PHY_measurements.rx_power_avg[eNB_id] = (int)
          (((k1*((long long int)(phy_vars_ue->PHY_measurements.rx_power_avg[eNB_id]))) +
            (k2*((long long int)(phy_vars_ue->PHY_measurements.rx_power_tot[eNB_id]))))>>10);

    phy_vars_ue->PHY_measurements.n0_power_avg = (int)
        (((k1*((long long int) (phy_vars_ue->PHY_measurements.n0_power_avg))) +
          (k2*((long long int) (phy_vars_ue->PHY_measurements.n0_power_tot))))>>10);
  } else {
    for (eNB_id = 0; eNB_id < phy_vars_ue->n_connected_eNB; eNB_id++)
      phy_vars_ue->PHY_measurements.rx_power_avg[eNB_id] = phy_vars_ue->PHY_measurements.rx_power_tot[eNB_id];

    phy_vars_ue->PHY_measurements.n0_power_avg = phy_vars_ue->PHY_measurements.n0_power_tot;
    phy_vars_ue->init_averaging = 0;
  }

  for (eNB_id = 0; eNB_id < phy_vars_ue->n_connected_eNB; eNB_id++) {
    phy_vars_ue->PHY_measurements.rx_power_avg_dB[eNB_id] = dB_fixed( phy_vars_ue->PHY_measurements.rx_power_avg[eNB_id]);
    phy_vars_ue->PHY_measurements.wideband_cqi_tot[eNB_id] = dB_fixed2(phy_vars_ue->PHY_measurements.rx_power_tot[eNB_id],phy_vars_ue->PHY_measurements.n0_power_tot);
    phy_vars_ue->PHY_measurements.wideband_cqi_avg[eNB_id] = dB_fixed2(phy_vars_ue->PHY_measurements.rx_power_avg[eNB_id],phy_vars_ue->PHY_measurements.n0_power_avg);
    phy_vars_ue->PHY_measurements.rx_rssi_dBm[eNB_id] = phy_vars_ue->PHY_measurements.rx_power_avg_dB[eNB_id] - phy_vars_ue->rx_total_gain_dB;
#ifdef DEBUG_MEAS
    LOG_I(PHY,"[eNB %d] lte_ue_measurements: RSSI %d dBm, RSSI (digital) %d dB\n",
          eNB_id,phy_vars_ue->PHY_measurements.rx_rssi_dBm[eNB_id],
          phy_vars_ue->PHY_measurements.rx_power_avg_dB[eNB_id]);
#endif
  }

  phy_vars_ue->PHY_measurements.n0_power_avg_dB = dB_fixed( phy_vars_ue->PHY_measurements.n0_power_avg);

  for (eNB_id = 0; eNB_id < phy_vars_ue->n_connected_eNB; eNB_id++) {
    if (frame_parms->mode1_flag==0) {
      // cqi/pmi information

      for (aarx=0; aarx<frame_parms->nb_antennas_rx; aarx++) {
        dl_ch0    = &phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][aarx][4];
        dl_ch1    = &phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][2+aarx][4];

        for (subband=0; subband<nb_subbands; subband++) {

          // cqi
          if (aarx==0)
            phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband]=0;

          if ((subband<(nb_subbands-1))||(N_RB_DL==6)) {
            /*for (i=0;i<48;i++)
            msg("subband %d (%d) : %d,%d\n",subband,i,((short *)dl_ch0)[2*i],((short *)dl_ch0)[1+(2*i)]);
            */
            phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband] =
              (signal_energy_nodc(dl_ch0,subband_size) + signal_energy_nodc(dl_ch1,subband_size));

            if ( phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband] < 0)
              phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband]=0;

            /*
            else
            phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband]-=phy_vars_ue->PHY_measurements.n0_power[aarx];
            */

            phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband] += phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband];
            phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][aarx][subband] = dB_fixed2(phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband],
                phy_vars_ue->PHY_measurements.n0_power[aarx]);
          } else { // this is for the last subband which is smaller in size
            //      for (i=0;i<12;i++)
            //        printf("subband %d (%d) : %d,%d\n",subband,i,((short *)dl_ch0)[2*i],((short *)dl_ch0)[1+(2*i)]);
            phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband] = (signal_energy_nodc(dl_ch0,last_subband_size) +
                signal_energy_nodc(dl_ch1,last_subband_size)); // - phy_vars_ue->PHY_measurements.n0_power[aarx];
            phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband] += phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband];
            phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][aarx][subband] = dB_fixed2(phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband],
                phy_vars_ue->PHY_measurements.n0_power[aarx]);
          }

          dl_ch1+=subband_size;
          dl_ch0+=subband_size;
          //    msg("subband_cqi[%d][%d][%d] => %d (%d dB)\n",eNB_id,aarx,subband,phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband],phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][aarx][subband]);
        }

      }

      for (subband=0; subband<nb_subbands; subband++) {
        phy_vars_ue->PHY_measurements.subband_cqi_tot_dB[eNB_id][subband] = dB_fixed2(phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband],phy_vars_ue->PHY_measurements.n0_power_tot);
        //    msg("subband_cqi_tot[%d][%d] => %d dB (n0 %d)\n",eNB_id,subband,phy_vars_ue->PHY_measurements.subband_cqi_tot_dB[eNB_id][subband],phy_vars_ue->PHY_measurements.n0_power_tot);
      }

      for (aarx=0; aarx<frame_parms->nb_antennas_rx; aarx++) {
        // skip the first 4 RE due to interpolation filter length of 5 (not possible to skip 5 due to 128i alignment, must be multiple of 128bit)

#if defined(__x86_64__) || defined(__i386__)
       __m128i pmi128_re,pmi128_im,mmtmpPMI0,mmtmpPMI1 /* ,mmtmpPMI2,mmtmpPMI3 */ ;

        dl_ch0_128    = (__m128i *)&phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][aarx][4];
        dl_ch1_128    = (__m128i *)&phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][2+aarx][4];
#elif defined(__arm__)
        int32x4_t pmi128_re,pmi128_im,mmtmpPMI0,mmtmpPMI1,mmtmpPMI0b,mmtmpPMI1b;

        dl_ch0_128    = (int16x8_t *)&phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][aarx][4];
        dl_ch1_128    = (int16x8_t *)&phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][2+aarx][4];

#endif
        for (subband=0; subband<nb_subbands; subband++) {


          // pmi
#if defined(__x86_64__) || defined(__i386__)
          pmi128_re = _mm_setzero_si128();
          pmi128_im = _mm_setzero_si128();
#elif defined(__arm__)
          pmi128_re = vdupq_n_s32(0);
	  pmi128_im = vdupq_n_s32(0);
#endif
          // limit is the number of groups of 4 REs in a subband (12 = 4 RBs, 3 = 1 RB)
          // for 5 MHz channelization, there are 7 subbands, 6 of size 4 RBs and 1 of size 1 RB
          if ((N_RB_DL==6) || (subband<(nb_subbands-1)))
            limit = subband_size>>2;
          else
            limit = last_subband_size>>2;

          for (i=0; i<limit; i++) {

            // For each RE in subband perform ch0 * conj(ch1)
            // multiply by conjugated channel
#if defined(__x86_64__) || defined(__i386__)
            mmtmpPMI1 = _mm_shufflelo_epi16(dl_ch1_128[0],_MM_SHUFFLE(2,3,0,1));//_MM_SHUFFLE(2,3,0,1)
            mmtmpPMI1 = _mm_shufflehi_epi16(mmtmpPMI1,_MM_SHUFFLE(2,3,0,1));
            mmtmpPMI1 = _mm_sign_epi16(mmtmpPMI1,*(__m128i*)&conjugate[0]);
            mmtmpPMI1 = _mm_madd_epi16(mmtmpPMI1,dl_ch0_128[0]);
            // mmtmpPMI1 contains imag part of 4 consecutive outputs (32-bit)

            pmi128_re = _mm_add_epi32(pmi128_re,mmtmpPMI0);
            pmi128_im = _mm_add_epi32(pmi128_im,mmtmpPMI1);
#elif defined(__arm__)
            mmtmpPMI0 = vmull_s16(((int16x4_t*)dl_ch0_128)[0], ((int16x4_t*)dl_ch1_128)[0]);
            mmtmpPMI1 = vmull_s16(((int16x4_t*)dl_ch0_128)[1], ((int16x4_t*)dl_ch1_128)[1]);
            pmi128_re = vqaddq_s32(pmi128_re,vcombine_s32(vpadd_s32(vget_low_s32(mmtmpPMI0),vget_high_s32(mmtmpPMI0)),vpadd_s32(vget_low_s32(mmtmpPMI1),vget_high_s32(mmtmpPMI1))));

            mmtmpPMI0b = vmull_s16(vrev32_s16(vmul_s16(((int16x4_t*)dl_ch0_128)[0],*(int16x4_t*)conjugate)), ((int16x4_t*)dl_ch1_128)[0]);
            mmtmpPMI1b = vmull_s16(vrev32_s16(vmul_s16(((int16x4_t*)dl_ch0_128)[1],*(int16x4_t*)conjugate)), ((int16x4_t*)dl_ch1_128)[1]);
            pmi128_im = vqaddq_s32(pmi128_im,vcombine_s32(vpadd_s32(vget_low_s32(mmtmpPMI0b),vget_high_s32(mmtmpPMI0b)),vpadd_s32(vget_low_s32(mmtmpPMI1b),vget_high_s32(mmtmpPMI1b))));

#endif
            dl_ch0_128++;
            dl_ch1_128++;
          }

          phy_vars_ue->PHY_measurements.subband_pmi_re[eNB_id][subband][aarx] = (((int *)&pmi128_re)[0] + ((int *)&pmi128_re)[1] + ((int *)&pmi128_re)[2] + ((int *)&pmi128_re)[3])>>2;
          phy_vars_ue->PHY_measurements.subband_pmi_im[eNB_id][subband][aarx] = (((int *)&pmi128_im)[0] + ((int *)&pmi128_im)[1] + ((int *)&pmi128_im)[2] + ((int *)&pmi128_im)[3])>>2;
          phy_vars_ue->PHY_measurements.wideband_pmi_re[eNB_id][aarx] += phy_vars_ue->PHY_measurements.subband_pmi_re[eNB_id][subband][aarx];
          phy_vars_ue->PHY_measurements.wideband_pmi_im[eNB_id][aarx] += phy_vars_ue->PHY_measurements.subband_pmi_im[eNB_id][subband][aarx];
        } // subband loop
      } // rx antenna loop
    }  // if frame_parms->mode1_flag == 0
    else {
      // cqi information only for mode 1
      for (aarx=0; aarx<frame_parms->nb_antennas_rx; aarx++) {
        dl_ch0    = &phy_vars_ue->lte_ue_common_vars.dl_ch_estimates[eNB_id][aarx][4];

        for (subband=0; subband<7; subband++) {

          // cqi
          if (aarx==0)
            phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband]=0;

          if (subband<6) {
            //      for (i=0;i<48;i++)
            //        printf("subband %d (%d) : %d,%d\n",subband,i,((short *)dl_ch0)[2*i],((short *)dl_ch0)[1+(2*i)]);
            phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband] =
              (signal_energy_nodc(dl_ch0,48) ) - phy_vars_ue->PHY_measurements.n0_power[aarx];

            phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband] += phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband];
            phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][aarx][subband] = dB_fixed2(phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband],
                phy_vars_ue->PHY_measurements.n0_power[aarx]);
          } else {
            //      for (i=0;i<12;i++)
            //        printf("subband %d (%d) : %d,%d\n",subband,i,((short *)dl_ch0)[2*i],((short *)dl_ch0)[1+(2*i)]);
            phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband] = (signal_energy_nodc(dl_ch0,12) ) - phy_vars_ue->PHY_measurements.n0_power[aarx];
            phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband] += phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband];
            phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][aarx][subband] = dB_fixed2(phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband],
                phy_vars_ue->PHY_measurements.n0_power[aarx]);
          }

          dl_ch1+=48;
          //    msg("subband_cqi[%d][%d][%d] => %d (%d dB)\n",eNB_id,aarx,subband,phy_vars_ue->PHY_measurements.subband_cqi[eNB_id][aarx][subband],phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][aarx][subband]);
        }
      }

      for (subband=0; subband<nb_subbands; subband++) {
        phy_vars_ue->PHY_measurements.subband_cqi_tot_dB[eNB_id][subband] = dB_fixed2(phy_vars_ue->PHY_measurements.subband_cqi_tot[eNB_id][subband],phy_vars_ue->PHY_measurements.n0_power_tot);
      }
    }

    phy_vars_ue->PHY_measurements.rank[eNB_id] = 0;

    for (i=0; i<nb_subbands; i++) {
      phy_vars_ue->PHY_measurements.selected_rx_antennas[eNB_id][i] = 0;

      if (frame_parms->nb_antennas_rx>1) {
        if (phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][0][i] >= phy_vars_ue->PHY_measurements.subband_cqi_dB[eNB_id][1][i])
          phy_vars_ue->PHY_measurements.selected_rx_antennas[eNB_id][i] = 0;
        else
          phy_vars_ue->PHY_measurements.selected_rx_antennas[eNB_id][i] = 1;
      } else
        phy_vars_ue->PHY_measurements.selected_rx_antennas[eNB_id][i] = 0;
    }

    // if(eNB_id==0)
    // printf("in lte_ue_measurements: selected rx_antenna[eNB_id==0]:%u\n", phy_vars_ue->PHY_measurements.selected_rx_antennas[eNB_id][i]);
  }  // eNB_id loop

#if defined(__x86_64__) || defined(__i386__)
  _mm_empty();
  _m_empty();
#endif
}


void lte_ue_measurements_emul(PHY_VARS_UE *phy_vars_ue,uint8_t last_slot,uint8_t eNB_id)
{

  msg("[PHY] EMUL UE lte_ue_measurements_emul last slot %d, eNB_id %d\n",last_slot,eNB_id);

 





